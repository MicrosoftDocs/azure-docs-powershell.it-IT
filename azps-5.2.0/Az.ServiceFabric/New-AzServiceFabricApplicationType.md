---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347791"
---
# <span data-ttu-id="d52a1-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="d52a1-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="d52a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d52a1-102">SYNOPSIS</span></span>
<span data-ttu-id="d52a1-103">Creare un nuovo tipo di applicazione in tessuto del servizio sotto il gruppo e il cluster di risorse specificati.</span><span class="sxs-lookup"><span data-stu-id="d52a1-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="d52a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d52a1-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d52a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d52a1-105">DESCRIPTION</span></span>
<span data-ttu-id="d52a1-106">Il cmdlet crea un nuovo tipo di applicazione tessuto di servizio sotto il gruppo di risorse e il cluster specificati.</span><span class="sxs-lookup"><span data-stu-id="d52a1-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="d52a1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d52a1-107">EXAMPLES</span></span>

### <span data-ttu-id="d52a1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d52a1-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="d52a1-109">In questo esempio verrà creato un nuovo tipo di applicazione "testAppType" sotto il gruppo di risorse e il cluster specificato.</span><span class="sxs-lookup"><span data-stu-id="d52a1-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="d52a1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d52a1-110">PARAMETERS</span></span>

### <span data-ttu-id="d52a1-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d52a1-111">-ClusterName</span></span>
<span data-ttu-id="d52a1-112">Specificare il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="d52a1-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="d52a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d52a1-113">-DefaultProfile</span></span>
<span data-ttu-id="d52a1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d52a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d52a1-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="d52a1-115">-Name</span></span>
<span data-ttu-id="d52a1-116">Specificare il nome del tipo di applicazione</span><span class="sxs-lookup"><span data-stu-id="d52a1-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="d52a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d52a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="d52a1-118">Specificare il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d52a1-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="d52a1-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d52a1-119">-Confirm</span></span>
<span data-ttu-id="d52a1-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d52a1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d52a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d52a1-121">-WhatIf</span></span>
<span data-ttu-id="d52a1-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d52a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d52a1-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d52a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d52a1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d52a1-124">CommonParameters</span></span>
<span data-ttu-id="d52a1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d52a1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d52a1-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d52a1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d52a1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d52a1-127">INPUTS</span></span>

### <span data-ttu-id="d52a1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d52a1-128">System.String</span></span>

## <span data-ttu-id="d52a1-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d52a1-129">OUTPUTS</span></span>

### <span data-ttu-id="d52a1-130">Microsoft. Azure. Commands. ServiceFabric. Models. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="d52a1-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="d52a1-131">Note</span><span class="sxs-lookup"><span data-stu-id="d52a1-131">NOTES</span></span>

## <span data-ttu-id="d52a1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d52a1-132">RELATED LINKS</span></span>
