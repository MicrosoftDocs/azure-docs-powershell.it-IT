---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlInstancePool.md
ms.openlocfilehash: 1b4f405e9bf6377855439d1f6d3cad9f0538920f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200131"
---
# <span data-ttu-id="ee2a7-101">New-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="ee2a7-101">New-AzSqlInstancePool</span></span>

## <span data-ttu-id="ee2a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee2a7-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2a7-103">Crea un pool di istanze di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-103">Creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ee2a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee2a7-104">SYNTAX</span></span>

```
New-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> -Location <String> -SubnetId <String>
 -VCore <Int32> -Edition <String> -ComputeGeneration <String> -LicenseType <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee2a7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee2a7-105">DESCRIPTION</span></span>
<span data-ttu-id="ee2a7-106">Il cmdlet **New-AzSqlInstancePool** crea un pool di istanze SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-106">The **New-AzSqlInstancePool** cmdlet creates an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ee2a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee2a7-107">EXAMPLES</span></span>

### <span data-ttu-id="ee2a7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee2a7-108">Example 1</span></span>
```powershell
PS C:\> New-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0 -Location canadacentral -SubnetId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name" -VCore 8 -Edition GeneralPurpose -ComputeGeneration Gen5 -LicenseType LicenseIncluded
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="ee2a7-109">Questo comando crea un nuovo pool di istanze di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-109">This command creates a new Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ee2a7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee2a7-110">PARAMETERS</span></span>

### <span data-ttu-id="ee2a7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee2a7-111">-AsJob</span></span>
<span data-ttu-id="ee2a7-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ee2a7-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee2a7-113">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ee2a7-113">-ComputeGeneration</span></span>
<span data-ttu-id="ee2a7-114">Generazione di COMPUTE per il pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-114">The compute generation for the instance pool.</span></span>

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

### <span data-ttu-id="ee2a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2a7-115">-DefaultProfile</span></span>
<span data-ttu-id="ee2a7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee2a7-117">-Edition</span><span class="sxs-lookup"><span data-stu-id="ee2a7-117">-Edition</span></span>
<span data-ttu-id="ee2a7-118">L'edizione per il pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-118">The edition for the instance pool.</span></span>

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

### <span data-ttu-id="ee2a7-119">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ee2a7-119">-LicenseType</span></span>
<span data-ttu-id="ee2a7-120">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-120">Determines which License Type to use.</span></span>
<span data-ttu-id="ee2a7-121">I valori possibili sono BasePrice (con sconto AHB) e LicenseIncluded (senza sconto AHB).</span><span class="sxs-lookup"><span data-stu-id="ee2a7-121">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="ee2a7-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ee2a7-122">-Location</span></span>
<span data-ttu-id="ee2a7-123">La posizione per creare il pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-123">The location to create the instance pool.</span></span>

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

### <span data-ttu-id="ee2a7-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee2a7-124">-Name</span></span>
<span data-ttu-id="ee2a7-125">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-125">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2a7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee2a7-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee2a7-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="ee2a7-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ee2a7-128">-SubnetId</span></span>
<span data-ttu-id="ee2a7-129">ID subnet da usare per la creazione di pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-129">The subnet id to use for instance pool creation.</span></span>

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

### <span data-ttu-id="ee2a7-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee2a7-130">-Tag</span></span>
<span data-ttu-id="ee2a7-131">Tag da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="ee2a7-131">The tags to associate with the instance</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2a7-132">-VCore</span><span class="sxs-lookup"><span data-stu-id="ee2a7-132">-VCore</span></span>
<span data-ttu-id="ee2a7-133">Determina la quantità di VCore da associare all'istanza.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-133">Determines how much VCore to associate with instance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: VCores

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2a7-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee2a7-134">-Confirm</span></span>
<span data-ttu-id="ee2a7-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee2a7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2a7-136">-WhatIf</span></span>
<span data-ttu-id="ee2a7-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee2a7-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee2a7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2a7-139">CommonParameters</span></span>
<span data-ttu-id="ee2a7-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee2a7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2a7-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee2a7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2a7-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee2a7-142">INPUTS</span></span>

### <span data-ttu-id="ee2a7-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ee2a7-143">None</span></span>

## <span data-ttu-id="ee2a7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee2a7-144">OUTPUTS</span></span>

### <span data-ttu-id="ee2a7-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="ee2a7-145">System.Object</span></span>
## <span data-ttu-id="ee2a7-146">Note</span><span class="sxs-lookup"><span data-stu-id="ee2a7-146">NOTES</span></span>

## <span data-ttu-id="ee2a7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee2a7-147">RELATED LINKS</span></span>