---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 498dec77dfc2f4ede8ae81aa70b10acfe2ad2954
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300913"
---
# <span data-ttu-id="0fa78-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0fa78-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="0fa78-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fa78-102">SYNOPSIS</span></span>
<span data-ttu-id="0fa78-103">Rimuovere il tessuto di servizio una versione del tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="0fa78-103">Remove Service fabric an application type version from the cluster.</span></span>

## <span data-ttu-id="0fa78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fa78-104">SYNTAX</span></span>

### <span data-ttu-id="0fa78-105">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0fa78-105">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fa78-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0fa78-106">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fa78-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0fa78-107">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fa78-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fa78-108">DESCRIPTION</span></span>
<span data-ttu-id="0fa78-109">Questo cmdlet rimuove il tessuto di servizio una versione del tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="0fa78-109">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="0fa78-110">Tutte le applicazioni in questa risorsa devono essere rimosse prima di eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="0fa78-110">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="0fa78-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fa78-111">EXAMPLES</span></span>

### <span data-ttu-id="0fa78-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0fa78-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="0fa78-113">In questo esempio viene rimossa la versione "V1" sotto il tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="0fa78-113">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="0fa78-114">Ci sono tutte le applicazioni in questa risorsa il comando genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="0fa78-114">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="0fa78-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fa78-115">PARAMETERS</span></span>

### <span data-ttu-id="0fa78-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0fa78-116">-ClusterName</span></span>
<span data-ttu-id="0fa78-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0fa78-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0fa78-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fa78-118">-DefaultProfile</span></span>
<span data-ttu-id="0fa78-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0fa78-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fa78-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0fa78-120">-Force</span></span>
<span data-ttu-id="0fa78-121">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="0fa78-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="0fa78-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fa78-122">-InputObject</span></span>
<span data-ttu-id="0fa78-123">Risorsa della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0fa78-123">The application type version resource.</span></span>

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

### <span data-ttu-id="0fa78-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fa78-124">-Name</span></span>
<span data-ttu-id="0fa78-125">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0fa78-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="0fa78-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fa78-126">-PassThru</span></span>
<span data-ttu-id="0fa78-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0fa78-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0fa78-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fa78-128">-ResourceGroupName</span></span>
<span data-ttu-id="0fa78-129">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fa78-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0fa78-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fa78-130">-ResourceId</span></span>
<span data-ttu-id="0fa78-131">ARM ResourceId della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0fa78-131">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="0fa78-132">-Versione</span><span class="sxs-lookup"><span data-stu-id="0fa78-132">-Version</span></span>
<span data-ttu-id="0fa78-133">Specifica la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0fa78-133">Specify the application type version.</span></span>

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

### <span data-ttu-id="0fa78-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0fa78-134">-Confirm</span></span>
<span data-ttu-id="0fa78-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fa78-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fa78-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fa78-136">-WhatIf</span></span>
<span data-ttu-id="0fa78-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fa78-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fa78-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fa78-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fa78-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fa78-139">CommonParameters</span></span>
<span data-ttu-id="0fa78-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fa78-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fa78-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0fa78-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fa78-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fa78-142">INPUTS</span></span>

### <span data-ttu-id="0fa78-143">System. String</span><span class="sxs-lookup"><span data-stu-id="0fa78-143">System.String</span></span>

### <span data-ttu-id="0fa78-144">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="0fa78-144">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="0fa78-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fa78-145">OUTPUTS</span></span>

### <span data-ttu-id="0fa78-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0fa78-146">System.Boolean</span></span>

## <span data-ttu-id="0fa78-147">Note</span><span class="sxs-lookup"><span data-stu-id="0fa78-147">NOTES</span></span>

## <span data-ttu-id="0fa78-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fa78-148">RELATED LINKS</span></span>
