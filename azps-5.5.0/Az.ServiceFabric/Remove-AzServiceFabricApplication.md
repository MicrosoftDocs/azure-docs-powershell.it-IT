---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183478"
---
# <span data-ttu-id="35268-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="35268-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="35268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35268-102">SYNOPSIS</span></span>
<span data-ttu-id="35268-103">Rimuovere un'applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="35268-103">Remove an application from the cluster.</span></span> <span data-ttu-id="35268-104">Tutti i servizi dell'applicazione verranno così rimosso.</span><span class="sxs-lookup"><span data-stu-id="35268-104">This will remove all the services under the application.</span></span> <span data-ttu-id="35268-105">Supporta solo ARM applicazioni distribuite.</span><span class="sxs-lookup"><span data-stu-id="35268-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="35268-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35268-106">SYNTAX</span></span>

### <span data-ttu-id="35268-107">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35268-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35268-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="35268-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35268-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="35268-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35268-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35268-110">DESCRIPTION</span></span>
<span data-ttu-id="35268-111">Questo cmdlet rimuove un'applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="35268-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="35268-112">Tutti i servizi, se presenti, verranno rimosso dalla risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35268-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="35268-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35268-113">EXAMPLES</span></span>

### <span data-ttu-id="35268-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35268-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="35268-115">Questo esempio rimuove l'applicazione "testApp" nel gruppo di risorse "testRG" e nel cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="35268-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="35268-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35268-116">PARAMETERS</span></span>

### <span data-ttu-id="35268-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="35268-117">-ClusterName</span></span>
<span data-ttu-id="35268-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="35268-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="35268-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35268-119">-DefaultProfile</span></span>
<span data-ttu-id="35268-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35268-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35268-121">-Force</span><span class="sxs-lookup"><span data-stu-id="35268-121">-Force</span></span>
<span data-ttu-id="35268-122">Rimuovere senza richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="35268-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="35268-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35268-123">-InputObject</span></span>
<span data-ttu-id="35268-124">Risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35268-124">The application resource.</span></span>

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

### <span data-ttu-id="35268-125">-Name</span><span class="sxs-lookup"><span data-stu-id="35268-125">-Name</span></span>
<span data-ttu-id="35268-126">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35268-126">Specify the name of the application.</span></span>

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

### <span data-ttu-id="35268-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35268-127">-PassThru</span></span>
<span data-ttu-id="35268-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="35268-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="35268-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35268-129">-ResourceGroupName</span></span>
<span data-ttu-id="35268-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="35268-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="35268-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35268-131">-ResourceId</span></span>
<span data-ttu-id="35268-132">Arm ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35268-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="35268-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35268-133">-Confirm</span></span>
<span data-ttu-id="35268-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35268-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35268-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35268-135">-WhatIf</span></span>
<span data-ttu-id="35268-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35268-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35268-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35268-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35268-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35268-138">CommonParameters</span></span>
<span data-ttu-id="35268-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35268-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35268-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35268-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35268-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="35268-141">INPUTS</span></span>

### <span data-ttu-id="35268-142">System.String</span><span class="sxs-lookup"><span data-stu-id="35268-142">System.String</span></span>

### <span data-ttu-id="35268-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span><span class="sxs-lookup"><span data-stu-id="35268-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="35268-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35268-144">OUTPUTS</span></span>

### <span data-ttu-id="35268-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="35268-145">System.Boolean</span></span>

## <span data-ttu-id="35268-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="35268-146">NOTES</span></span>

## <span data-ttu-id="35268-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35268-147">RELATED LINKS</span></span>
