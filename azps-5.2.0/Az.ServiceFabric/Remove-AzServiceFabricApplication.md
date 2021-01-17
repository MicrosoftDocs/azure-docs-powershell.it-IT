---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricApplication.md
ms.openlocfilehash: 7dbd9df3e6bd87aedcfeb80964959553bac8deca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348604"
---
# <span data-ttu-id="af9b8-101">Remove-AzServiceFabricApplication</span><span class="sxs-lookup"><span data-stu-id="af9b8-101">Remove-AzServiceFabricApplication</span></span>

## <span data-ttu-id="af9b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af9b8-102">SYNOPSIS</span></span>
<span data-ttu-id="af9b8-103">Rimuovere un'applicazione dal cluster.</span><span class="sxs-lookup"><span data-stu-id="af9b8-103">Remove an application from the cluster.</span></span> <span data-ttu-id="af9b8-104">Verranno rimossi tutti i servizi sotto l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="af9b8-104">This will remove all the services under the application.</span></span> <span data-ttu-id="af9b8-105">Supporta solo le applicazioni distribuite ARM.</span><span class="sxs-lookup"><span data-stu-id="af9b8-105">Only supports ARM deployed applications.</span></span>

## <span data-ttu-id="af9b8-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af9b8-106">SYNTAX</span></span>

### <span data-ttu-id="af9b8-107">ByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af9b8-107">ByResourceGroup (Default)</span></span>
```
Remove-AzServiceFabricApplication [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9b8-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="af9b8-108">ByResourceId</span></span>
```
Remove-AzServiceFabricApplication -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af9b8-109">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="af9b8-109">ByInputObject</span></span>
```
Remove-AzServiceFabricApplication -InputObject <PSApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af9b8-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af9b8-110">DESCRIPTION</span></span>
<span data-ttu-id="af9b8-111">Questo cmdlet consente di rimuovere un modulo di applicazione il cluster.</span><span class="sxs-lookup"><span data-stu-id="af9b8-111">This cmdlet removes an application form the cluster.</span></span> <span data-ttu-id="af9b8-112">In questo modo verranno rimossi tutti i servizi, se presenti, nella risorsa applicazione.</span><span class="sxs-lookup"><span data-stu-id="af9b8-112">This will remove all the services, if any, under the application resource.</span></span>

## <span data-ttu-id="af9b8-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af9b8-113">EXAMPLES</span></span>

### <span data-ttu-id="af9b8-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af9b8-114">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appName = "testApp"
PS C:\> Remove-AzServiceFabricApplication -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appName
```

<span data-ttu-id="af9b8-115">In questo esempio viene rimossa l'applicazione "testApp" nel gruppo di risorse "testRG" e il cluster "testCluster".</span><span class="sxs-lookup"><span data-stu-id="af9b8-115">This example removes the application "testApp" under the resource group "testRG" and cluster "testCluster".</span></span>

## <span data-ttu-id="af9b8-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af9b8-116">PARAMETERS</span></span>

### <span data-ttu-id="af9b8-117">-Clustername</span><span class="sxs-lookup"><span data-stu-id="af9b8-117">-ClusterName</span></span>
<span data-ttu-id="af9b8-118">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="af9b8-118">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="af9b8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9b8-119">-DefaultProfile</span></span>
<span data-ttu-id="af9b8-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af9b8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9b8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="af9b8-121">-Force</span></span>
<span data-ttu-id="af9b8-122">Rimuovi senza richiesta.</span><span class="sxs-lookup"><span data-stu-id="af9b8-122">Remove without prompt.</span></span>

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

### <span data-ttu-id="af9b8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af9b8-123">-InputObject</span></span>
<span data-ttu-id="af9b8-124">Risorsa dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="af9b8-124">The application resource.</span></span>

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

### <span data-ttu-id="af9b8-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="af9b8-125">-Name</span></span>
<span data-ttu-id="af9b8-126">Specificare il nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="af9b8-126">Specify the name of the application.</span></span>

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

### <span data-ttu-id="af9b8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="af9b8-127">-PassThru</span></span>
<span data-ttu-id="af9b8-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="af9b8-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="af9b8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9b8-129">-ResourceGroupName</span></span>
<span data-ttu-id="af9b8-130">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="af9b8-130">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="af9b8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af9b8-131">-ResourceId</span></span>
<span data-ttu-id="af9b8-132">ARM ResourceId dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="af9b8-132">Arm ResourceId of the application.</span></span>

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

### <span data-ttu-id="af9b8-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af9b8-133">-Confirm</span></span>
<span data-ttu-id="af9b8-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af9b8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af9b8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af9b8-135">-WhatIf</span></span>
<span data-ttu-id="af9b8-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af9b8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af9b8-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af9b8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af9b8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9b8-138">CommonParameters</span></span>
<span data-ttu-id="af9b8-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9b8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9b8-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af9b8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9b8-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af9b8-141">INPUTS</span></span>

### <span data-ttu-id="af9b8-142">System. String</span><span class="sxs-lookup"><span data-stu-id="af9b8-142">System.String</span></span>

### <span data-ttu-id="af9b8-143">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="af9b8-143">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplication</span></span>

## <span data-ttu-id="af9b8-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af9b8-144">OUTPUTS</span></span>

### <span data-ttu-id="af9b8-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="af9b8-145">System.Boolean</span></span>

## <span data-ttu-id="af9b8-146">Note</span><span class="sxs-lookup"><span data-stu-id="af9b8-146">NOTES</span></span>

## <span data-ttu-id="af9b8-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af9b8-147">RELATED LINKS</span></span>
