---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98485851"
---
# <span data-ttu-id="891c0-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="891c0-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="891c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="891c0-102">SYNOPSIS</span></span>
<span data-ttu-id="891c0-103">Rimuovere un'applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="891c0-103">Remove an application from the cluster.</span></span> <span data-ttu-id="891c0-104">Verranno rimossi tutti i servizi sotto l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="891c0-104">This will remove all the services under the application.</span></span> <span data-ttu-id="891c0-105">Supporta solo le applicazioni distribuite ARM.</span><span class="sxs-lookup"><span data-stu-id="891c0-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="891c0-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="891c0-106">SYNTAX</span></span>

### <span data-ttu-id="891c0-107">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="891c0-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="891c0-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="891c0-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="891c0-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="891c0-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="891c0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="891c0-110">DESCRIPTION</span></span>
<span data-ttu-id="891c0-111">Questo cmdlet consente di rimuovere un modulo di applicazione il cluster.</span><span class="sxs-lookup"><span data-stu-id="891c0-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="891c0-112">In questo modo verranno rimossi tutti i servizi, se presenti, nella risorsa applicazione.</span><span class="sxs-lookup"><span data-stu-id="891c0-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="891c0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="891c0-113">EXAMPLES</span></span>

### <span data-ttu-id="891c0-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="891c0-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="891c0-115">In questo esempio viene rimossa l'applicazione "testApp" nel gruppo di risorse "testRG" e il cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="891c0-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="891c0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="891c0-116">PARAMETERS</span></span>

### <span data-ttu-id="891c0-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="891c0-117">-ClusterName</span></span>
<span data-ttu-id="891c0-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="891c0-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="891c0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="891c0-119">-DefaultProfile</span></span>
<span data-ttu-id="891c0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="891c0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="891c0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="891c0-121">-Force</span></span>
<span data-ttu-id="891c0-122">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="891c0-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="891c0-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="891c0-123">-InputObject</span></span>
<span data-ttu-id="891c0-124">Risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="891c0-124">The application resource.</span></span>

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

### <span data-ttu-id="891c0-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="891c0-125">-Name</span></span>
<span data-ttu-id="891c0-126">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="891c0-126">Specify the name of the application.</span></span>

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

### <span data-ttu-id="891c0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="891c0-127">-PassThru</span></span>
<span data-ttu-id="891c0-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="891c0-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="891c0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="891c0-129">-ResourceGroupName</span></span>
<span data-ttu-id="891c0-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="891c0-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="891c0-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="891c0-131">-ResourceId</span></span>
<span data-ttu-id="891c0-132">ARM ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="891c0-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="891c0-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="891c0-133">-Confirm</span></span>
<span data-ttu-id="891c0-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="891c0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="891c0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="891c0-135">-WhatIf</span></span>
<span data-ttu-id="891c0-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="891c0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="891c0-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="891c0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="891c0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891c0-138">CommonParameters</span></span>
<span data-ttu-id="891c0-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="891c0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891c0-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="891c0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891c0-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="891c0-141">INPUTS</span></span>

### <span data-ttu-id="891c0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="891c0-142">System.String</span></span>

### <span data-ttu-id="891c0-143">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="891c0-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="891c0-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="891c0-144">OUTPUTS</span></span>

### <span data-ttu-id="891c0-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="891c0-145">System.Boolean</span></span>

## <span data-ttu-id="891c0-146">Note</span><span class="sxs-lookup"><span data-stu-id="891c0-146">NOTES</span></span>

## <span data-ttu-id="891c0-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="891c0-147">RELATED LINKS</span></span>
