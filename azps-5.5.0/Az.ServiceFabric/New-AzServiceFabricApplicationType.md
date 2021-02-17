---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198655"
---
# <span data-ttu-id="5225b-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="5225b-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="5225b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5225b-102">SYNOPSIS</span></span>
<span data-ttu-id="5225b-103">Creare un nuovo tipo di applicazione tessuto di servizio nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="5225b-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="5225b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5225b-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5225b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5225b-105">DESCRIPTION</span></span>
<span data-ttu-id="5225b-106">Il cmdlet crea un nuovo tipo di applicazione infrastruttura di servizio nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="5225b-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="5225b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5225b-107">EXAMPLES</span></span>

### <span data-ttu-id="5225b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5225b-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="5225b-109">Questo esempio creerà un nuovo tipo di applicazione "testAppType" nel gruppo di risorse e nel cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="5225b-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="5225b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5225b-110">PARAMETERS</span></span>

### <span data-ttu-id="5225b-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="5225b-111">-ClusterName</span></span>
<span data-ttu-id="5225b-112">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="5225b-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5225b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5225b-113">-DefaultProfile</span></span>
<span data-ttu-id="5225b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5225b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5225b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5225b-115">-Name</span></span>
<span data-ttu-id="5225b-116">Specificare il nome del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="5225b-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5225b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5225b-117">-ResourceGroupName</span></span>
<span data-ttu-id="5225b-118">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5225b-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5225b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5225b-119">-Confirm</span></span>
<span data-ttu-id="5225b-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5225b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5225b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5225b-121">-WhatIf</span></span>
<span data-ttu-id="5225b-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5225b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5225b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5225b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5225b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5225b-124">CommonParameters</span></span>
<span data-ttu-id="5225b-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5225b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5225b-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5225b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5225b-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="5225b-127">INPUTS</span></span>

### <span data-ttu-id="5225b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5225b-128">System.String</span></span>

## <span data-ttu-id="5225b-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5225b-129">OUTPUTS</span></span>

### <span data-ttu-id="5225b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="5225b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="5225b-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="5225b-131">NOTES</span></span>

## <span data-ttu-id="5225b-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5225b-132">RELATED LINKS</span></span>
