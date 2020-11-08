---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: f50baca10d3079ac800b694670ce2b4c8c85fc84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019639"
---
# <span data-ttu-id="83b6b-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="83b6b-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="83b6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="83b6b-103">Rimuovere il tessuto di servizio una versione del tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="83b6b-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="83b6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83b6b-104">SYNTAX</span></span>

### <span data-ttu-id="83b6b-105">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83b6b-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83b6b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83b6b-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83b6b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83b6b-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83b6b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83b6b-108">DESCRIPTION</span></span>
<span data-ttu-id="83b6b-109">Questo cmdlet rimuove il tessuto di servizio una versione del tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="83b6b-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="83b6b-110">Tutte le applicazioni in questa risorsa devono essere rimosse prima di eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="83b6b-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="83b6b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83b6b-111">EXAMPLES</span></span>

### <span data-ttu-id="83b6b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="83b6b-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="83b6b-113">In questo esempio viene rimossa la versione "V1" sotto il tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="83b6b-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="83b6b-114">Ci sono tutte le applicazioni in questa risorsa il comando genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="83b6b-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="83b6b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83b6b-115">PARAMETERS</span></span>

### <span data-ttu-id="83b6b-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="83b6b-116">-ClusterName</span></span>
<span data-ttu-id="83b6b-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="83b6b-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="83b6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83b6b-118">-DefaultProfile</span></span>
<span data-ttu-id="83b6b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83b6b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83b6b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="83b6b-120">-Force</span></span>
<span data-ttu-id="83b6b-121">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="83b6b-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="83b6b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83b6b-122">-InputObject</span></span>
<span data-ttu-id="83b6b-123">Risorsa della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="83b6b-123">The application type version resource.</span></span>

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

### <span data-ttu-id="83b6b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="83b6b-124">-Name</span></span>
<span data-ttu-id="83b6b-125">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="83b6b-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="83b6b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83b6b-126">-PassThru</span></span>
<span data-ttu-id="83b6b-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="83b6b-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="83b6b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83b6b-128">-ResourceGroupName</span></span>
<span data-ttu-id="83b6b-129">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83b6b-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="83b6b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83b6b-130">-ResourceId</span></span>
<span data-ttu-id="83b6b-131">ARM ResourceId della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="83b6b-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="83b6b-132">-Versione</span><span class="sxs-lookup"><span data-stu-id="83b6b-132">-Version</span></span>
<span data-ttu-id="83b6b-133">Specifica la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="83b6b-133">Specify the application type version.</span></span>

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

### <span data-ttu-id="83b6b-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83b6b-134">-Confirm</span></span>
<span data-ttu-id="83b6b-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83b6b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83b6b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83b6b-136">-WhatIf</span></span>
<span data-ttu-id="83b6b-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b6b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83b6b-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83b6b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83b6b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83b6b-139">CommonParameters</span></span>
<span data-ttu-id="83b6b-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83b6b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83b6b-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83b6b-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83b6b-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83b6b-142">INPUTS</span></span>

### <span data-ttu-id="83b6b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="83b6b-143">System.String</span></span>

### <span data-ttu-id="83b6b-144">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="83b6b-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="83b6b-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83b6b-145">OUTPUTS</span></span>

### <span data-ttu-id="83b6b-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="83b6b-146">System.Boolean</span></span>

## <span data-ttu-id="83b6b-147">Note</span><span class="sxs-lookup"><span data-stu-id="83b6b-147">NOTES</span></span>

## <span data-ttu-id="83b6b-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83b6b-148">RELATED LINKS</span></span>
