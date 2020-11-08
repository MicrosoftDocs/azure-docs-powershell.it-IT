---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Kusto.dll-Help.xml
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Remove-AzKustoDatabase.md
ms.openlocfilehash: 47b519b324018e4fc369d281f7fb7eac554ac571
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019085"
---
# <span data-ttu-id="3c4ff-101">Remove-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="3c4ff-101">Remove-AzKustoDatabase</span></span>

## <span data-ttu-id="3c4ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3c4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="3c4ff-103">Elimina un database di Kusto esistente.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-103">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="3c4ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3c4ff-104">SYNTAX</span></span>

### <span data-ttu-id="3c4ff-105">ByNameAndResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3c4ff-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzKustoDatabase [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c4ff-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3c4ff-106">ByResourceId</span></span>
```
Remove-AzKustoDatabase [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c4ff-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3c4ff-107">ByInputObject</span></span>
```
Remove-AzKustoDatabase [-InputObject] <PSKustoDatabase> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c4ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c4ff-108">DESCRIPTION</span></span>
<span data-ttu-id="3c4ff-109">Elimina un database di Kusto esistente.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-109">Deletes an existing Kusto database.</span></span>

## <span data-ttu-id="3c4ff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3c4ff-110">EXAMPLES</span></span>

### <span data-ttu-id="3c4ff-111">Esempio 1-eliminare un database di Kusto esistente in base al nome</span><span class="sxs-lookup"><span data-stu-id="3c4ff-111">Example 1 - Delete an existing Kusto database by name</span></span>

```
PS C:\> Remove-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase
```

<span data-ttu-id="3c4ff-112">Il comando precedente elimina il database kusto denominato "mykustodatabase" nel cluster "mykustocluster" disponibile nel gruppo risorse "testrg".</span><span class="sxs-lookup"><span data-stu-id="3c4ff-112">The above command deletes the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="3c4ff-113">Esempio 2-eliminare un database di Kusto esistente tramite piping</span><span class="sxs-lookup"><span data-stu-id="3c4ff-113">Example 2 - Delete an existing Kusto database by piping</span></span>

```
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName mykustocluster -Name mykustodatabase | Remove-AzKustoDatabase
```

<span data-ttu-id="3c4ff-114">Il comando precedente ottiene il database kusto denominato "mykustodatabase" nel cluster "mykustocluster" trovato nel gruppo di risorse "testrg" con il `Get-AzKustoDatabase` cmdlet e quindi convoglia il risultato per `Remove-AzKustoDatabase` eliminarlo.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-114">The above command gets the Kusto database named "mykustodatabase" in the cluster "mykustocluster" found in the resource group "testrg" using the `Get-AzKustoDatabase` cmdlet, and then pipes the result to `Remove-AzKustoDatabase` to delete it.</span></span>

## <span data-ttu-id="3c4ff-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3c4ff-115">PARAMETERS</span></span>

### <span data-ttu-id="3c4ff-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="3c4ff-116">-ClusterName</span></span>
<span data-ttu-id="3c4ff-117">Nome del cluster in cui è presente il database.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-117">Name of the cluster under which the database exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c4ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c4ff-118">-DefaultProfile</span></span>
<span data-ttu-id="3c4ff-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c4ff-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c4ff-120">-InputObject</span></span>
<span data-ttu-id="3c4ff-121">Oggetto di database kusto.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-121">Kusto database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c4ff-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c4ff-122">-Name</span></span>
<span data-ttu-id="3c4ff-123">Nome del database da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-123">Name of database to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c4ff-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c4ff-124">-PassThru</span></span>
<span data-ttu-id="3c4ff-125">Restituirà se il database specificato è stato sospeso o meno.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-125">Return whether the specified database was successfully suspended or not.</span></span>

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

### <span data-ttu-id="3c4ff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c4ff-126">-ResourceGroupName</span></span>
<span data-ttu-id="3c4ff-127">Nome del gruppo di risorse in cui è presente il cluster.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-127">Name of resource group under which the cluster exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c4ff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c4ff-128">-ResourceId</span></span>
<span data-ttu-id="3c4ff-129">ResourceID database kusto.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-129">Kusto database ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c4ff-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3c4ff-130">-Confirm</span></span>
<span data-ttu-id="3c4ff-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c4ff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c4ff-132">-WhatIf</span></span>
<span data-ttu-id="3c4ff-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c4ff-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c4ff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c4ff-135">CommonParameters</span></span>
<span data-ttu-id="3c4ff-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c4ff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c4ff-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c4ff-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c4ff-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3c4ff-138">INPUTS</span></span>

### <span data-ttu-id="3c4ff-139">System. String</span><span class="sxs-lookup"><span data-stu-id="3c4ff-139">System.String</span></span>

### <span data-ttu-id="3c4ff-140">Microsoft. Azure. Commands. kusto. Models. PSKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="3c4ff-140">Microsoft.Azure.Commands.Kusto.Models.PSKustoDatabase</span></span>

## <span data-ttu-id="3c4ff-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3c4ff-141">OUTPUTS</span></span>

### <span data-ttu-id="3c4ff-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c4ff-142">System.Boolean</span></span>

## <span data-ttu-id="3c4ff-143">Note</span><span class="sxs-lookup"><span data-stu-id="3c4ff-143">NOTES</span></span>

## <span data-ttu-id="3c4ff-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3c4ff-144">RELATED LINKS</span></span>
