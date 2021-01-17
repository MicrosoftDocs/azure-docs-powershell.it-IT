---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: db7d9165b8aec6a69f31850f7a37eddb2450e53b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475442"
---
# <span data-ttu-id="6c4b6-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="6c4b6-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="6c4b6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c4b6-102">SYNOPSIS</span></span>
<span data-ttu-id="6c4b6-103">Imposta le proprietà per un pool di istanze di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="6c4b6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c4b6-104">SYNTAX</span></span>

### <span data-ttu-id="6c4b6-105">DefaultSetInstancePoolParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6c4b6-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c4b6-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c4b6-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c4b6-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c4b6-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c4b6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c4b6-108">DESCRIPTION</span></span>
<span data-ttu-id="6c4b6-109">Il cmdlet **set-AzSqlInstancePool** modifica le proprietà di un pool di istanze SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="6c4b6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c4b6-110">EXAMPLES</span></span>

### <span data-ttu-id="6c4b6-111">Esempio 1: impostare un tipo di licenza per pool di istanze</span><span class="sxs-lookup"><span data-stu-id="6c4b6-111">Example 1 : Set an instance pool license type</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0 -LicenseType LicenseIncluded
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

<span data-ttu-id="6c4b6-112">Questo comando imposta il tipo di licenza e/o i tag per un pool di istanze denominato instancePool0.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="6c4b6-113">Esempio 2: impostare un tipo di licenza per pool di istanze usando un oggetto pool di istanze</span><span class="sxs-lookup"><span data-stu-id="6c4b6-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
PS C:\> Set-AzSqlInstancePool -InputObject $instancePool -LicenseType LicenseIncluded
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

<span data-ttu-id="6c4b6-114">Questo comando imposta il tipo di licenza e/o i tag per un pool di istanze usando un oggetto pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="6c4b6-115">Esempio 3: impostare un tipo di licenza per pool di istanze usando un ID risorsa di pool di istanze</span><span class="sxs-lookup"><span data-stu-id="6c4b6-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
```powershell
PS C:\> Set-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0" -LicenseType LicenseIncluded
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

<span data-ttu-id="6c4b6-116">Questo comando imposta il tipo di licenza e/o i tag per un pool di istanze denominato instancePool0.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="6c4b6-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c4b6-117">PARAMETERS</span></span>

### <span data-ttu-id="6c4b6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c4b6-118">-AsJob</span></span>
<span data-ttu-id="6c4b6-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6c4b6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6c4b6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c4b6-120">-DefaultProfile</span></span>
<span data-ttu-id="6c4b6-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c4b6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c4b6-122">-InputObject</span></span>
<span data-ttu-id="6c4b6-123">Oggetto di input del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-123">The instance pool input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InputObjectSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b6-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="6c4b6-124">-LicenseType</span></span>
<span data-ttu-id="6c4b6-125">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-125">Determines which License Type to use.</span></span>
<span data-ttu-id="6c4b6-126">I valori possibili sono BasePrice (con sconto AHB) e LicenseIncluded (senza sconto AHB).</span><span class="sxs-lookup"><span data-stu-id="6c4b6-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="6c4b6-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c4b6-127">-Name</span></span>
<span data-ttu-id="6c4b6-128">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-128">The name of the instance pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c4b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="6c4b6-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c4b6-131">-ResourceId</span></span>
<span data-ttu-id="6c4b6-132">Identificatore delle risorse del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-132">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetInstancePoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c4b6-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="6c4b6-133">-Tag</span></span>
<span data-ttu-id="6c4b6-134">Tag da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="6c4b6-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="6c4b6-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6c4b6-135">-Confirm</span></span>
<span data-ttu-id="6c4b6-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c4b6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c4b6-137">-WhatIf</span></span>
<span data-ttu-id="6c4b6-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c4b6-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c4b6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c4b6-140">CommonParameters</span></span>
<span data-ttu-id="6c4b6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c4b6-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c4b6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c4b6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c4b6-143">INPUTS</span></span>

### <span data-ttu-id="6c4b6-144">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="6c4b6-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="6c4b6-145">System. String</span><span class="sxs-lookup"><span data-stu-id="6c4b6-145">System.String</span></span>

## <span data-ttu-id="6c4b6-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c4b6-146">OUTPUTS</span></span>

### <span data-ttu-id="6c4b6-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="6c4b6-147">System.Object</span></span>
## <span data-ttu-id="6c4b6-148">Note</span><span class="sxs-lookup"><span data-stu-id="6c4b6-148">NOTES</span></span>

## <span data-ttu-id="6c4b6-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c4b6-149">RELATED LINKS</span></span>
