---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: 8ba56568a10ee8223a53bc1530602f3ae930e14c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98485843"
---
# <span data-ttu-id="ecc79-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="ecc79-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="ecc79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecc79-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc79-103">Rimuovere il tessuto del servizio un tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="ecc79-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="ecc79-104">In questo modo verranno rimosse tutte le versioni di tipo in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="ecc79-104">This will remove all type versions under this resource.</span></span> <span data-ttu-id="ecc79-105">Supporta solo i tipi di applicazione distribuiti ARM.</span><span class="sxs-lookup"><span data-stu-id="ecc79-105">Only supports ARM deployed application types.</span></span>

## <span data-ttu-id="ecc79-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecc79-106">SYNTAX</span></span>

### <span data-ttu-id="ecc79-107">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ecc79-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecc79-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ecc79-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ecc79-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ecc79-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecc79-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecc79-110">DESCRIPTION</span></span>
<span data-ttu-id="ecc79-111">Questo cmdlet rimuove un tipo di applicazione il cluster e rimuoverà tutta la versione del tipo in questa risorsa, ma tutte le applicazioni in essa devono essere rimosse prima di eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="ecc79-111">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="ecc79-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecc79-112">EXAMPLES</span></span>

### <span data-ttu-id="ecc79-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ecc79-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="ecc79-114">In questo esempio verrà rimosso il tipo di applicazione "testAppType" e tutta la versione sotto di essa.</span><span class="sxs-lookup"><span data-stu-id="ecc79-114">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="ecc79-115">Se sono state create applicazioni con questo tipo, il comando genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="ecc79-115">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="ecc79-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecc79-116">PARAMETERS</span></span>

### <span data-ttu-id="ecc79-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="ecc79-117">-ClusterName</span></span>
<span data-ttu-id="ecc79-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="ecc79-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="ecc79-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc79-119">-DefaultProfile</span></span>
<span data-ttu-id="ecc79-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc79-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecc79-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ecc79-121">-Force</span></span>
<span data-ttu-id="ecc79-122">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="ecc79-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="ecc79-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecc79-123">-InputObject</span></span>
<span data-ttu-id="ecc79-124">Risorsa tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="ecc79-124">The application type resource.</span></span>

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

### <span data-ttu-id="ecc79-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecc79-125">-Name</span></span>
<span data-ttu-id="ecc79-126">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="ecc79-126">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="ecc79-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecc79-127">-PassThru</span></span>
<span data-ttu-id="ecc79-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ecc79-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ecc79-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecc79-129">-ResourceGroupName</span></span>
<span data-ttu-id="ecc79-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ecc79-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="ecc79-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecc79-131">-ResourceId</span></span>
<span data-ttu-id="ecc79-132">ARM ResourceId del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="ecc79-132">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="ecc79-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ecc79-133">-Confirm</span></span>
<span data-ttu-id="ecc79-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc79-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecc79-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc79-135">-WhatIf</span></span>
<span data-ttu-id="ecc79-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecc79-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecc79-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecc79-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecc79-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc79-138">CommonParameters</span></span>
<span data-ttu-id="ecc79-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc79-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc79-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecc79-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc79-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecc79-141">INPUTS</span></span>

### <span data-ttu-id="ecc79-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ecc79-142">System.String</span></span>

### <span data-ttu-id="ecc79-143">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="ecc79-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="ecc79-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecc79-144">OUTPUTS</span></span>

### <span data-ttu-id="ecc79-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ecc79-145">System.Boolean</span></span>

## <span data-ttu-id="ecc79-146">Note</span><span class="sxs-lookup"><span data-stu-id="ecc79-146">NOTES</span></span>

## <span data-ttu-id="ecc79-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecc79-147">RELATED LINKS</span></span>
