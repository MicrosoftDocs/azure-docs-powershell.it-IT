---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtypeversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationTypeVersion.md
ms.openlocfilehash: 5ab0499ce3fe98a541031b78e2b432de5a2a39dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98485856"
---
# <span data-ttu-id="41222-101">Remove-AzServiceFabricApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="41222-101">Remove-AzServiceFabricApplicationTypeVersion</span></span>

## <span data-ttu-id="41222-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="41222-102">SYNOPSIS</span></span>
<span data-ttu-id="41222-103">Rimuovere il tessuto di servizio una versione del tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="41222-103">Remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="41222-104">Supporta solo le versioni di tipo applicazione distribuite ARM.</span><span class="sxs-lookup"><span data-stu-id="41222-104">Only supports ARM deployed application type versions.</span></span>

## <span data-ttu-id="41222-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="41222-105">SYNTAX</span></span>

### <span data-ttu-id="41222-106">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="41222-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion [-ResourceGroupName] <String> [-ClusterName] <String>
 -Name <String> -Version <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41222-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="41222-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41222-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="41222-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationTypeVersion -InputObject <PSApplicationTypeVersion> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41222-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41222-109">DESCRIPTION</span></span>
<span data-ttu-id="41222-110">Questo cmdlet rimuove il tessuto di servizio una versione del tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="41222-110">This cmdlet will remove Service fabric an application type version from the cluster.</span></span> <span data-ttu-id="41222-111">Tutte le applicazioni in questa risorsa devono essere rimosse prima di eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="41222-111">All applications under this resource must be removed before running this command.</span></span>

## <span data-ttu-id="41222-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="41222-112">EXAMPLES</span></span>

### <span data-ttu-id="41222-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="41222-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $version = "v1"
PS C:\> Remove-AzServiceFabricApplicationTypeVersion -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Version $version -Force -PassThru -Verbose
```

<span data-ttu-id="41222-114">In questo esempio viene rimossa la versione "V1" sotto il tipo "testAppType".</span><span class="sxs-lookup"><span data-stu-id="41222-114">This example will remove the version "v1" under the type "testAppType".</span></span> <span data-ttu-id="41222-115">Ci sono tutte le applicazioni in questa risorsa il comando genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="41222-115">It there are any applications under this resource the command will throw an exception.</span></span>

## <span data-ttu-id="41222-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="41222-116">PARAMETERS</span></span>

### <span data-ttu-id="41222-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="41222-117">-ClusterName</span></span>
<span data-ttu-id="41222-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="41222-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="41222-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41222-119">-DefaultProfile</span></span>
<span data-ttu-id="41222-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="41222-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41222-121">-Force</span><span class="sxs-lookup"><span data-stu-id="41222-121">-Force</span></span>
<span data-ttu-id="41222-122">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="41222-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="41222-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41222-123">-InputObject</span></span>
<span data-ttu-id="41222-124">Risorsa della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="41222-124">The application type version resource.</span></span>

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

### <span data-ttu-id="41222-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="41222-125">-Name</span></span>
<span data-ttu-id="41222-126">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="41222-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="41222-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41222-127">-PassThru</span></span>
<span data-ttu-id="41222-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="41222-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="41222-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41222-129">-ResourceGroupName</span></span>
<span data-ttu-id="41222-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="41222-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="41222-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41222-131">-ResourceId</span></span>
<span data-ttu-id="41222-132">ARM ResourceId della versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="41222-132">Arm ResourceId of the application type version.</span></span>

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

### <span data-ttu-id="41222-133">-Versione</span><span class="sxs-lookup"><span data-stu-id="41222-133">-Version</span></span>
<span data-ttu-id="41222-134">Specifica la versione del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="41222-134">Specify the application type version.</span></span>

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

### <span data-ttu-id="41222-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="41222-135">-Confirm</span></span>
<span data-ttu-id="41222-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41222-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41222-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41222-137">-WhatIf</span></span>
<span data-ttu-id="41222-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41222-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41222-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="41222-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41222-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41222-140">CommonParameters</span></span>
<span data-ttu-id="41222-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41222-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41222-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41222-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41222-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="41222-143">INPUTS</span></span>

### <span data-ttu-id="41222-144">System. String</span><span class="sxs-lookup"><span data-stu-id="41222-144">System.String</span></span>

### <span data-ttu-id="41222-145">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationTypeVersion</span><span class="sxs-lookup"><span data-stu-id="41222-145">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationTypeVersion</span></span>

## <span data-ttu-id="41222-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="41222-146">OUTPUTS</span></span>

### <span data-ttu-id="41222-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="41222-147">System.Boolean</span></span>

## <span data-ttu-id="41222-148">Note</span><span class="sxs-lookup"><span data-stu-id="41222-148">NOTES</span></span>

## <span data-ttu-id="41222-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="41222-149">RELATED LINKS</span></span>
