---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: 07a7e8c656fb028b9db813201ac2628da294209b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971741"
---
# <span data-ttu-id="ab7d9-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="ab7d9-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="ab7d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab7d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7d9-103">Restituisce informazioni sull'utilizzo di un pool SQL istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="ab7d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab7d9-104">SYNTAX</span></span>

### <span data-ttu-id="ab7d9-105">InstancePoolUsageDefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab7d9-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab7d9-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab7d9-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab7d9-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab7d9-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab7d9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ab7d9-108">DESCRIPTION</span></span>
<span data-ttu-id="ab7d9-109">Il cmdlet **Get-AzSqlInstancePoolUsage** restituisce informazioni sull'utilizzo del pool di SQL di istanza di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="ab7d9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab7d9-110">EXAMPLES</span></span>

### <span data-ttu-id="ab7d9-111">Esempio 1: ottiene l'uso di un pool di istanze SQL Azure</span><span class="sxs-lookup"><span data-stu-id="ab7d9-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="ab7d9-112">Ottiene l'utilizzo per il pool di SQL di istanza di Azure0.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="ab7d9-113">Esempio 2: Ottiene l'uso di un pool di istanze SQL Azure usando un oggetto pool di istanze</span><span class="sxs-lookup"><span data-stu-id="ab7d9-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> Get-AzSqlInstancePoolUsage -InstancePool $instancePool

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="ab7d9-114">Ottiene l'utilizzo per il pool di istanze SQL Azure con un oggetto pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="ab7d9-115">Esempio 3: Ottiene l'uso di un pool di istanze di Azure SQL usando un ID risorsa pool di istanze</span><span class="sxs-lookup"><span data-stu-id="ab7d9-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="ab7d9-116">Ottiene l'uso per il pool di SQL istanza di Azure con un identificatore di risorsa del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="ab7d9-117">Esempio 3: Ottiene l'uso di un pool di istanze SQL Azure con un'analisi degli utilizzi delle istanze gestite all'interno del pool.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0 -ExpandChildren

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/vcore_utilization
CurrentValue   :
Limit          : 2
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/storage_utilization
CurrentValue   :
Limit          : 32
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages
```

<span data-ttu-id="ab7d9-118">Ottiene l'utilizzo per il pool di istanze SQL Azure e per gli utilizzi delle istanze gestite all'interno di instancepool0.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="ab7d9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab7d9-119">PARAMETERS</span></span>

### <span data-ttu-id="ab7d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab7d9-120">-DefaultProfile</span></span>
<span data-ttu-id="ab7d9-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab7d9-122">-Expand Expand</span><span class="sxs-lookup"><span data-stu-id="ab7d9-122">-ExpandChildren</span></span>
<span data-ttu-id="ab7d9-123">Flag che indica se espandere l'utilizzo del pool di istanze con l'uso dei relativi figli.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

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

### <span data-ttu-id="ab7d9-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="ab7d9-124">-InstancePool</span></span>
<span data-ttu-id="ab7d9-125">Oggetto pool di istanze padre.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-125">The parent instance pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InstancePoolUsageParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7d9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ab7d9-126">-Name</span></span>
<span data-ttu-id="ab7d9-127">Nome del pool di istanze gestite.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-127">The managed instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7d9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab7d9-128">-ResourceGroupName</span></span>
<span data-ttu-id="ab7d9-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7d9-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab7d9-130">-ResourceId</span></span>
<span data-ttu-id="ab7d9-131">ID risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-131">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageResourceIdParameterSet
Aliases: InstancePoolResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7d9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7d9-132">CommonParameters</span></span>
<span data-ttu-id="ab7d9-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7d9-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab7d9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7d9-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ab7d9-135">INPUTS</span></span>

### <span data-ttu-id="ab7d9-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="ab7d9-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="ab7d9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ab7d9-137">System.String</span></span>

## <span data-ttu-id="ab7d9-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab7d9-138">OUTPUTS</span></span>

### <span data-ttu-id="ab7d9-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span><span class="sxs-lookup"><span data-stu-id="ab7d9-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="ab7d9-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="ab7d9-140">NOTES</span></span>

## <span data-ttu-id="ab7d9-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab7d9-141">RELATED LINKS</span></span>
