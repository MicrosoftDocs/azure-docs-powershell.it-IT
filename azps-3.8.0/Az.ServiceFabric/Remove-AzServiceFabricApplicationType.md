---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplicationType.md
ms.openlocfilehash: bba2ab235532f83b3955ff9a12016438e0e1960e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019642"
---
# <span data-ttu-id="0723a-101">Remove-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="0723a-101">Remove-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="0723a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0723a-102">SYNOPSIS</span></span>
<span data-ttu-id="0723a-103">Rimuovere il tessuto del servizio un tipo di applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="0723a-103">Remove Service fabric an application type from the cluster.</span></span> <span data-ttu-id="0723a-104">In questo modo verranno rimosse tutte le versioni di tipo in questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="0723a-104">This will remove all type versions under this resource.</span></span>

## <span data-ttu-id="0723a-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0723a-105">SYNTAX</span></span>

### <span data-ttu-id="0723a-106">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0723a-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String>]
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0723a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0723a-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplicationType -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0723a-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0723a-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplicationType -InputObject <PSApplicationType> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0723a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0723a-109">DESCRIPTION</span></span>
<span data-ttu-id="0723a-110">Questo cmdlet rimuove un tipo di applicazione il cluster e rimuoverà tutta la versione del tipo in questa risorsa, ma tutte le applicazioni in essa devono essere rimosse prima di eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="0723a-110">This cmdlet removes an application type form the cluster and will remove all type version under this resource, but all applications under it should be removed before running this command.</span></span>

## <span data-ttu-id="0723a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0723a-111">EXAMPLES</span></span>

### <span data-ttu-id="0723a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0723a-112">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> Remove-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="0723a-113">In questo esempio verrà rimosso il tipo di applicazione "testAppType" e tutta la versione sotto di essa.</span><span class="sxs-lookup"><span data-stu-id="0723a-113">This example will remove the application type "testAppType" and all the version under it.</span></span> <span data-ttu-id="0723a-114">Se sono state create applicazioni con questo tipo, il comando genererà un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="0723a-114">If there are any applications created with this type, the command will throw an exception.</span></span>

## <span data-ttu-id="0723a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0723a-115">PARAMETERS</span></span>

### <span data-ttu-id="0723a-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="0723a-116">-ClusterName</span></span>
<span data-ttu-id="0723a-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="0723a-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="0723a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0723a-118">-DefaultProfile</span></span>
<span data-ttu-id="0723a-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0723a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0723a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="0723a-120">-Force</span></span>
<span data-ttu-id="0723a-121">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="0723a-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="0723a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0723a-122">-InputObject</span></span>
<span data-ttu-id="0723a-123">Risorsa tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0723a-123">The application type resource.</span></span>

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

### <span data-ttu-id="0723a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="0723a-124">-Name</span></span>
<span data-ttu-id="0723a-125">Specificare il nome del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0723a-125">Specify the name of the application type.</span></span>

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

### <span data-ttu-id="0723a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0723a-126">-PassThru</span></span>
<span data-ttu-id="0723a-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="0723a-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="0723a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0723a-128">-ResourceGroupName</span></span>
<span data-ttu-id="0723a-129">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0723a-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="0723a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0723a-130">-ResourceId</span></span>
<span data-ttu-id="0723a-131">ARM ResourceId del tipo di applicazione.</span><span class="sxs-lookup"><span data-stu-id="0723a-131">Arm ResourceId of the application type.</span></span>

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

### <span data-ttu-id="0723a-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0723a-132">-Confirm</span></span>
<span data-ttu-id="0723a-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0723a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0723a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0723a-134">-WhatIf</span></span>
<span data-ttu-id="0723a-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0723a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0723a-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0723a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0723a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0723a-137">CommonParameters</span></span>
<span data-ttu-id="0723a-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0723a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0723a-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0723a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0723a-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0723a-140">INPUTS</span></span>

### <span data-ttu-id="0723a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0723a-141">System.String</span></span>

### <span data-ttu-id="0723a-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="0723a-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="0723a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0723a-143">OUTPUTS</span></span>

### <span data-ttu-id="0723a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0723a-144">System.Boolean</span></span>

## <span data-ttu-id="0723a-145">Note</span><span class="sxs-lookup"><span data-stu-id="0723a-145">NOTES</span></span>

## <span data-ttu-id="0723a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0723a-146">RELATED LINKS</span></span>
