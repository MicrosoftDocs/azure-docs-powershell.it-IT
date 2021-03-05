---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 217666284a2245b79864bb6561a1f85143c1ae80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005565"
---
# <span data-ttu-id="e4521-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e4521-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="e4521-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4521-102">SYNOPSIS</span></span>
<span data-ttu-id="e4521-103">Rimuovere la versione service fabric di un tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="e4521-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="e4521-104">Supporta solo le ARM di tipi di applicazione distribuite.</span><span class="sxs-lookup"><span data-stu-id="e4521-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="e4521-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4521-105">SYNTAX</span></span>

### <span data-ttu-id="e4521-106">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4521-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4521-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e4521-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4521-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e4521-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4521-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e4521-109">DESCRIPTION</span></span>
<span data-ttu-id="e4521-110">Questo cmdlet rimuoverà la versione di un tipo di applicazione dell'infrastruttura del servizio dal cluster.</span><span class="sxs-lookup"><span data-stu-id="e4521-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="e4521-111">Prima di eseguire questo comando, tutte le applicazioni in questa risorsa devono essere rimosse.</span><span class="sxs-lookup"><span data-stu-id="e4521-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="e4521-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4521-112">EXAMPLES</span></span>

### <span data-ttu-id="e4521-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4521-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="e4521-114">Questo esempio rimuove la versione "v1" del tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="e4521-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="e4521-115">Il comando genera un'eccezione se sono presenti applicazioni in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4521-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="e4521-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4521-116">PARAMETERS</span></span>

### <span data-ttu-id="e4521-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e4521-117">-ClusterName</span></span>
<span data-ttu-id="e4521-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="e4521-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e4521-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4521-119">-DefaultProfile</span></span>
<span data-ttu-id="e4521-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4521-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4521-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e4521-121">-Force</span></span>
<span data-ttu-id="e4521-122">Rimuovere senza richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="e4521-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="e4521-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4521-123">-InputObject</span></span>
<span data-ttu-id="e4521-124">Risorsa versione tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="e4521-124">The application type version resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e4521-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e4521-125">-Name</span></span>
<span data-ttu-id="e4521-126">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="e4521-126">Specify the name of the application type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4521-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4521-127">-PassThru</span></span>
<span data-ttu-id="e4521-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="e4521-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="e4521-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4521-129">-ResourceGroupName</span></span>
<span data-ttu-id="e4521-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4521-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e4521-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4521-131">-ResourceId</span></span>
<span data-ttu-id="e4521-132">Arm ResourceId della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="e4521-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="e4521-133">-Version</span><span class="sxs-lookup"><span data-stu-id="e4521-133">-Version</span></span>
<span data-ttu-id="e4521-134">Specificare la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="e4521-134">Specify the application type version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationTypeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4521-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4521-135">-Confirm</span></span>
<span data-ttu-id="e4521-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4521-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4521-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4521-137">-WhatIf</span></span>
<span data-ttu-id="e4521-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4521-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4521-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4521-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4521-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4521-140">CommonParameters</span></span>
<span data-ttu-id="e4521-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4521-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4521-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e4521-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4521-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="e4521-143">INPUTS</span></span>

### <span data-ttu-id="e4521-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e4521-144">System.String</span></span>

### <span data-ttu-id="e4521-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="e4521-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="e4521-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4521-146">OUTPUTS</span></span>

### <span data-ttu-id="e4521-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e4521-147">System.Boolean</span></span>

## <span data-ttu-id="e4521-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="e4521-148">NOTES</span></span>

## <span data-ttu-id="e4521-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4521-149">RELATED LINKS</span></span>
