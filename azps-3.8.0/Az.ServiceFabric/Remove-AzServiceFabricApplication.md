---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: e9f248575d0f5193a11c729384e674870b3de29c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019650"
---
# <span data-ttu-id="c9f3c-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="c9f3c-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="c9f3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9f3c-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f3c-103">Rimuovere un'applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-103">Remove an application from the cluster.</span></span> <span data-ttu-id="c9f3c-104">Verranno rimossi tutti i servizi sotto l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-104">This will remove all the services under the application.</span></span>

## <span data-ttu-id="c9f3c-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9f3c-105">SYNTAX</span></span>

### <span data-ttu-id="c9f3c-106">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c9f3c-106">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f3c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c9f3c-107">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f3c-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c9f3c-108">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9f3c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9f3c-109">DESCRIPTION</span></span>
<span data-ttu-id="c9f3c-110">Questo cmdlet consente di rimuovere un modulo di applicazione il cluster.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-110">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="c9f3c-111">In questo modo verranno rimossi tutti i servizi, se presenti, nella risorsa applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-111">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="c9f3c-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9f3c-112">EXAMPLES</span></span>

### <span data-ttu-id="c9f3c-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c9f3c-113">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="c9f3c-114">In questo esempio viene rimossa l'applicazione "testApp" nel gruppo di risorse "testRG" e il cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="c9f3c-114">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="c9f3c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9f3c-115">PARAMETERS</span></span>

### <span data-ttu-id="c9f3c-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c9f3c-116">-ClusterName</span></span>
<span data-ttu-id="c9f3c-117">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-117">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="c9f3c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f3c-118">-DefaultProfile</span></span>
<span data-ttu-id="c9f3c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f3c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c9f3c-120">-Force</span></span>
<span data-ttu-id="c9f3c-121">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-121">Remove without prompt.</span></span>

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

### <span data-ttu-id="c9f3c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9f3c-122">-InputObject</span></span>
<span data-ttu-id="c9f3c-123">Risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-123">The application resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9f3c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9f3c-124">-Name</span></span>
<span data-ttu-id="c9f3c-125">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-125">Specify the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases: ApplicationName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9f3c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9f3c-126">-PassThru</span></span>
<span data-ttu-id="c9f3c-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c9f3c-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c9f3c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9f3c-128">-ResourceGroupName</span></span>
<span data-ttu-id="c9f3c-129">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-129">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="c9f3c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c9f3c-130">-ResourceId</span></span>
<span data-ttu-id="c9f3c-131">ARM ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-131">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="c9f3c-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c9f3c-132">-Confirm</span></span>
<span data-ttu-id="c9f3c-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f3c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f3c-134">-WhatIf</span></span>
<span data-ttu-id="c9f3c-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9f3c-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f3c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f3c-137">CommonParameters</span></span>
<span data-ttu-id="c9f3c-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f3c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f3c-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9f3c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f3c-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9f3c-140">INPUTS</span></span>

### <span data-ttu-id="c9f3c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c9f3c-141">System.String</span></span>

### <span data-ttu-id="c9f3c-142">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="c9f3c-142">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="c9f3c-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9f3c-143">OUTPUTS</span></span>

### <span data-ttu-id="c9f3c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9f3c-144">System.Boolean</span></span>

## <span data-ttu-id="c9f3c-145">Note</span><span class="sxs-lookup"><span data-stu-id="c9f3c-145">NOTES</span></span>

## <span data-ttu-id="c9f3c-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9f3c-146">RELATED LINKS</span></span>
