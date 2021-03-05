---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstancePool.md
ms.openlocfilehash: 0d7efa268709d0691fe55bfaf322bd9accf79dab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997119"
---
# <span data-ttu-id="d4640-101">Set-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="d4640-101">Set-AzSqlInstancePool</span></span>

## <span data-ttu-id="d4640-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4640-102">SYNOPSIS</span></span>
<span data-ttu-id="d4640-103">Imposta le proprietà per un pool di SQL azure.</span><span class="sxs-lookup"><span data-stu-id="d4640-103">Sets properties for an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="d4640-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4640-104">SYNTAX</span></span>

### <span data-ttu-id="d4640-105">DefaultSetInstancePoolParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d4640-105">DefaultSetInstancePoolParameterSet (Default)</span></span>
```
Set-AzSqlInstancePool [-ResourceGroupName] <String> [-Name] <String> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4640-106">InputObjectSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4640-106">InputObjectSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-InputObject] <AzureSqlInstancePoolModel> [-LicenseType <String>] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4640-107">ResourceIdSetInstancePoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="d4640-107">ResourceIdSetInstancePoolParameterSet</span></span>
```
Set-AzSqlInstancePool [-ResourceId] <String> [-LicenseType <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4640-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4640-108">DESCRIPTION</span></span>
<span data-ttu-id="d4640-109">Il cmdlet **Set-AzSqlInstancePool** modifica le proprietà di un pool di SQL azure.</span><span class="sxs-lookup"><span data-stu-id="d4640-109">The **Set-AzSqlInstancePool** cmdlet modifies properties of an Azure SQL Instance pool.</span></span>

## <span data-ttu-id="d4640-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4640-110">EXAMPLES</span></span>

### <span data-ttu-id="d4640-111">Esempio 1: Impostare un tipo di licenza per pool di istanze</span><span class="sxs-lookup"><span data-stu-id="d4640-111">Example 1 : Set an instance pool license type</span></span>
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

<span data-ttu-id="d4640-112">Questo comando imposta il tipo di licenza e/o i tag per un pool di istanze denominato istanzaPool0.</span><span class="sxs-lookup"><span data-stu-id="d4640-112">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

### <span data-ttu-id="d4640-113">Esempio 2: Impostare un tipo di licenza per pool di istanze usando un oggetto pool di istanze</span><span class="sxs-lookup"><span data-stu-id="d4640-113">Example 2 : Set an instance pool license type using an instance pool object</span></span>
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

<span data-ttu-id="d4640-114">Questo comando imposta il tipo di licenza e/o i tag per un pool di istanze usando un oggetto pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="d4640-114">This command sets the license type and/or tags for an instance pool using an instance pool object.</span></span>

### <span data-ttu-id="d4640-115">Esempio 3: Impostare un tipo di licenza per pool di istanze usando un ID risorsa pool di istanze</span><span class="sxs-lookup"><span data-stu-id="d4640-115">Example 3 : Set an instance pool license type using an instance pool resource id</span></span>
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

<span data-ttu-id="d4640-116">Questo comando imposta il tipo di licenza e/o i tag per un pool di istanze denominato istanzaPool0.</span><span class="sxs-lookup"><span data-stu-id="d4640-116">This command sets the license type and/or tags for an instance pool named instancePool0.</span></span>

## <span data-ttu-id="d4640-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4640-117">PARAMETERS</span></span>

### <span data-ttu-id="d4640-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4640-118">-AsJob</span></span>
<span data-ttu-id="d4640-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d4640-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4640-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4640-120">-DefaultProfile</span></span>
<span data-ttu-id="d4640-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4640-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4640-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4640-122">-InputObject</span></span>
<span data-ttu-id="d4640-123">Oggetto di input del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="d4640-123">The instance pool input object.</span></span>

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

### <span data-ttu-id="d4640-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d4640-124">-LicenseType</span></span>
<span data-ttu-id="d4640-125">Determina il tipo di licenza da usare.</span><span class="sxs-lookup"><span data-stu-id="d4640-125">Determines which License Type to use.</span></span>
<span data-ttu-id="d4640-126">I valori possibili sono PrezzoPrice (con sconto AHB) e LicenseIncluded (senza sconto AHB).</span><span class="sxs-lookup"><span data-stu-id="d4640-126">Possible values are BasePrice (with AHB discount) and LicenseIncluded (without AHB discount).</span></span>

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

### <span data-ttu-id="d4640-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d4640-127">-Name</span></span>
<span data-ttu-id="d4640-128">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="d4640-128">The name of the instance pool.</span></span>

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

### <span data-ttu-id="d4640-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4640-129">-ResourceGroupName</span></span>
<span data-ttu-id="d4640-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d4640-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4640-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4640-131">-ResourceId</span></span>
<span data-ttu-id="d4640-132">L'identificatore di risorsa del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="d4640-132">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="d4640-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4640-133">-Tag</span></span>
<span data-ttu-id="d4640-134">I tag da associare all'istanza</span><span class="sxs-lookup"><span data-stu-id="d4640-134">The tags to associate with the instance</span></span>

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

### <span data-ttu-id="d4640-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4640-135">-Confirm</span></span>
<span data-ttu-id="d4640-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4640-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4640-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4640-137">-WhatIf</span></span>
<span data-ttu-id="d4640-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4640-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4640-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d4640-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4640-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4640-140">CommonParameters</span></span>
<span data-ttu-id="d4640-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4640-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4640-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4640-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4640-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4640-143">INPUTS</span></span>

### <span data-ttu-id="d4640-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="d4640-144">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="d4640-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d4640-145">System.String</span></span>

## <span data-ttu-id="d4640-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4640-146">OUTPUTS</span></span>

### <span data-ttu-id="d4640-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="d4640-147">System.Object</span></span>
## <span data-ttu-id="d4640-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4640-148">NOTES</span></span>

## <span data-ttu-id="d4640-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4640-149">RELATED LINKS</span></span>
