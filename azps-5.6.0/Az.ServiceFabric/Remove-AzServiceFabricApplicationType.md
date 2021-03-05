---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: dbd2e29a3136576ecf5596c4a401d689fd0631a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005581"
---
# <span data-ttu-id="7c8b0-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="7c8b0-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="7c8b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c8b0-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8b0-103">Rimuovere un tipo di applicazione da un tipo di applicazione del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="7c8b0-104">In questo modo verranno rimuovono tutte le versioni dei tipi in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="7c8b0-105">Supporta solo i ARM di applicazioni distribuiti.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="7c8b0-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c8b0-106">SYNTAX</span></span>

### <span data-ttu-id="7c8b0-107">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c8b0-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8b0-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7c8b0-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c8b0-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7c8b0-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c8b0-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c8b0-110">DESCRIPTION</span></span>
<span data-ttu-id="7c8b0-111">Questo cmdlet rimuove un tipo di applicazione dal cluster e rimuove tutta la versione tipo in questa risorsa, ma tutte le applicazioni in esso installate devono essere rimosse prima di eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="7c8b0-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c8b0-112">EXAMPLES</span></span>

### <span data-ttu-id="7c8b0-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c8b0-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="7c8b0-114">Questo esempio rimuove il tipo di applicazione "testAppType" e tutte le versioni al di sotto.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="7c8b0-115">Se sono presenti applicazioni create con questo tipo, il comando genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="7c8b0-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c8b0-116">PARAMETERS</span></span>

### <span data-ttu-id="7c8b0-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="7c8b0-117">-ClusterName</span></span>
<span data-ttu-id="7c8b0-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="7c8b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8b0-119">-DefaultProfile</span></span>
<span data-ttu-id="7c8b0-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c8b0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7c8b0-121">-Force</span></span>
<span data-ttu-id="7c8b0-122">Rimuovere senza richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="7c8b0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c8b0-123">-InputObject</span></span>
<span data-ttu-id="7c8b0-124">Risorsa tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-124">The application type resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c8b0-125">-Name</span><span class="sxs-lookup"><span data-stu-id="7c8b0-125">-Name</span></span>
<span data-ttu-id="7c8b0-126">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c8b0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c8b0-127">-PassThru</span></span>
<span data-ttu-id="7c8b0-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7c8b0-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7c8b0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c8b0-129">-ResourceGroupName</span></span>
<span data-ttu-id="7c8b0-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="7c8b0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c8b0-131">-ResourceId</span></span>
<span data-ttu-id="7c8b0-132">Arm ResourceId del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="7c8b0-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c8b0-133">-Confirm</span></span>
<span data-ttu-id="7c8b0-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c8b0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c8b0-135">-WhatIf</span></span>
<span data-ttu-id="7c8b0-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c8b0-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c8b0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8b0-138">CommonParameters</span></span>
<span data-ttu-id="7c8b0-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8b0-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7c8b0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8b0-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c8b0-141">INPUTS</span></span>

### <span data-ttu-id="7c8b0-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7c8b0-142">System.String</span></span>

### <span data-ttu-id="7c8b0-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="7c8b0-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="7c8b0-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c8b0-144">OUTPUTS</span></span>

### <span data-ttu-id="7c8b0-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c8b0-145">System.Boolean</span></span>

## <span data-ttu-id="7c8b0-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c8b0-146">NOTES</span></span>

## <span data-ttu-id="7c8b0-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c8b0-147">RELATED LINKS</span></span>
