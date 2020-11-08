---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/New-AzKustoCluster.md
ms.openlocfilehash: 9c18597da52900794e5f891fb06385249c173a0b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019090"
---
# <span data-ttu-id="30e0c-101">New-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="30e0c-101">New-AzKustoCluster</span></span>

## <span data-ttu-id="30e0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30e0c-102">SYNOPSIS</span></span>
<span data-ttu-id="30e0c-103">Crea un nuovo cluster di Kusto.</span><span class="sxs-lookup"><span data-stu-id="30e0c-103">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="30e0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30e0c-104">SYNTAX</span></span>

```
New-AzKustoCluster [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-Tier <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30e0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30e0c-105">DESCRIPTION</span></span>
<span data-ttu-id="30e0c-106">Crea un nuovo cluster di Kusto.</span><span class="sxs-lookup"><span data-stu-id="30e0c-106">Creates a new Kusto cluster.</span></span>

## <span data-ttu-id="30e0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30e0c-107">EXAMPLES</span></span>

### <span data-ttu-id="30e0c-108">Esempio 1-creare un nuovo cluster di Kusto</span><span class="sxs-lookup"><span data-stu-id="30e0c-108">Example 1 - Create a new Kusto cluster</span></span>

```
PS C:\> New-AzKustoCluster -ResourceGroupName testrg -Name mykustocluster -Location 'Central US' -Sku D13_v2 -Capacity 10

Type              : Microsoft.Kusto/Clusters
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/mykustocluster
ResourceGroup     : testrg
Name              : mykustocluster
Location          : Central US
Capacity          : 10
Sku               : D13_v2
ProvisioningState : Succeeded
State             : Running
Tag               : {}
Uri               : https://mykustocluster.centralus.kusto.windows.net
DataIngestionUri  : https://ingest-mykustocluster.centralus.kusto.windows.net
```

<span data-ttu-id="30e0c-109">Il comando precedente crea un nuovo cluster di Kusto denominato "mykustocluster" nel gruppo di risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="30e0c-109">The above command creates a new Kusto cluster named "mykustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="30e0c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30e0c-110">PARAMETERS</span></span>

### <span data-ttu-id="30e0c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e0c-111">-DefaultProfile</span></span>
<span data-ttu-id="30e0c-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30e0c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30e0c-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="30e0c-113">-Location</span></span>
<span data-ttu-id="30e0c-114">Area di Azure in cui deve essere creato il cluster.</span><span class="sxs-lookup"><span data-stu-id="30e0c-114">Azure region where the cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e0c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="30e0c-115">-Name</span></span>
<span data-ttu-id="30e0c-116">Nome del cluster da creare.</span><span class="sxs-lookup"><span data-stu-id="30e0c-116">Name of the cluster to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e0c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30e0c-117">-ResourceGroupName</span></span>
<span data-ttu-id="30e0c-118">Nome del gruppo di risorse in cui si vuole creare il cluster.</span><span class="sxs-lookup"><span data-stu-id="30e0c-118">Name of resource group under which you want to create the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e0c-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="30e0c-119">-Sku</span></span>
<span data-ttu-id="30e0c-120">Nome dell'USK usato per creare il cluster</span><span class="sxs-lookup"><span data-stu-id="30e0c-120">Name of the Sku used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e0c-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="30e0c-121">-Tag</span></span>
<span data-ttu-id="30e0c-122">Stringa, dizionario di stringhe di tag associati al cluster</span><span class="sxs-lookup"><span data-stu-id="30e0c-122">A string,string dictionary of tags associated with this cluster</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e0c-123">-Tier</span><span class="sxs-lookup"><span data-stu-id="30e0c-123">-Tier</span></span>
<span data-ttu-id="30e0c-124">Nome del livello usato per creare il cluster</span><span class="sxs-lookup"><span data-stu-id="30e0c-124">Name of the Tier used to create the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e0c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30e0c-125">-Confirm</span></span>
<span data-ttu-id="30e0c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30e0c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30e0c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30e0c-127">-WhatIf</span></span>
<span data-ttu-id="30e0c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30e0c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30e0c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30e0c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30e0c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e0c-130">CommonParameters</span></span>
<span data-ttu-id="30e0c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30e0c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e0c-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e0c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e0c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30e0c-133">INPUTS</span></span>

### <span data-ttu-id="30e0c-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="30e0c-134">None</span></span>

## <span data-ttu-id="30e0c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30e0c-135">OUTPUTS</span></span>

### <span data-ttu-id="30e0c-136">Microsoft. Azure. Commands. kusto. Models. PSKustoCluster</span><span class="sxs-lookup"><span data-stu-id="30e0c-136">Microsoft.Azure.Commands.Kusto.Models.PSKustoCluster</span></span>

## <span data-ttu-id="30e0c-137">Note</span><span class="sxs-lookup"><span data-stu-id="30e0c-137">NOTES</span></span>

## <span data-ttu-id="30e0c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30e0c-138">RELATED LINKS</span></span>
