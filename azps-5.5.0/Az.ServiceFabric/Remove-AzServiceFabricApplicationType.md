---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183471"
---
# <span data-ttu-id="eb92c-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="eb92c-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="eb92c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eb92c-102">SYNOPSIS</span></span>
<span data-ttu-id="eb92c-103">Rimuovere un tipo di applicazione da un tipo di applicazione del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="eb92c-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="eb92c-104">In questo modo verranno rimuovono tutte le versioni del tipo in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="eb92c-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="eb92c-105">Supporta solo i ARM di applicazioni distribuiti.</span><span class="sxs-lookup"><span data-stu-id="eb92c-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="eb92c-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb92c-106">SYNTAX</span></span>

### <span data-ttu-id="eb92c-107">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eb92c-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb92c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb92c-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb92c-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb92c-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb92c-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eb92c-110">DESCRIPTION</span></span>
<span data-ttu-id="eb92c-111">Questo cmdlet rimuove un tipo di applicazione dal cluster e rimuove tutta la versione tipo in questa risorsa, ma tutte le applicazioni in esso installate devono essere rimosse prima di eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="eb92c-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="eb92c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb92c-112">EXAMPLES</span></span>

### <span data-ttu-id="eb92c-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eb92c-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="eb92c-114">Questo esempio rimuove il tipo di applicazione "testAppType" e tutte le versioni al di sotto.</span><span class="sxs-lookup"><span data-stu-id="eb92c-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="eb92c-115">Se sono presenti applicazioni create con questo tipo, il comando genera un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="eb92c-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="eb92c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eb92c-116">PARAMETERS</span></span>

### <span data-ttu-id="eb92c-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="eb92c-117">-ClusterName</span></span>
<span data-ttu-id="eb92c-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="eb92c-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="eb92c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb92c-119">-DefaultProfile</span></span>
<span data-ttu-id="eb92c-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb92c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb92c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="eb92c-121">-Force</span></span>
<span data-ttu-id="eb92c-122">Rimuovere senza richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="eb92c-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="eb92c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb92c-123">-InputObject</span></span>
<span data-ttu-id="eb92c-124">Risorsa tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb92c-124">The application type resource.</span></span>

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

### <span data-ttu-id="eb92c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="eb92c-125">-Name</span></span>
<span data-ttu-id="eb92c-126">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb92c-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="eb92c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb92c-127">-PassThru</span></span>
<span data-ttu-id="eb92c-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="eb92c-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="eb92c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb92c-129">-ResourceGroupName</span></span>
<span data-ttu-id="eb92c-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb92c-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="eb92c-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb92c-131">-ResourceId</span></span>
<span data-ttu-id="eb92c-132">Arm ResourceId del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="eb92c-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="eb92c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eb92c-133">-Confirm</span></span>
<span data-ttu-id="eb92c-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb92c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb92c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb92c-135">-WhatIf</span></span>
<span data-ttu-id="eb92c-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb92c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb92c-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb92c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb92c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb92c-138">CommonParameters</span></span>
<span data-ttu-id="eb92c-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb92c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb92c-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eb92c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb92c-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="eb92c-141">INPUTS</span></span>

### <span data-ttu-id="eb92c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="eb92c-142">System.String</span></span>

### <span data-ttu-id="eb92c-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="eb92c-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="eb92c-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb92c-144">OUTPUTS</span></span>

### <span data-ttu-id="eb92c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eb92c-145">System.Boolean</span></span>

## <span data-ttu-id="eb92c-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="eb92c-146">NOTES</span></span>

## <span data-ttu-id="eb92c-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb92c-147">RELATED LINKS</span></span>
