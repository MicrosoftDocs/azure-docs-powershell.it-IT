---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: c2acc357e53a57060f7ba1ff3e19a5344ceee412
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191882"
---
# <span data-ttu-id="a03ea-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="a03ea-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="a03ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a03ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a03ea-103">Restituisce informazioni sull'utilizzo di un pool di istanze di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a03ea-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="a03ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a03ea-104">SYNTAX</span></span>

### <span data-ttu-id="a03ea-105">InstancePoolUsageDefaultParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a03ea-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a03ea-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a03ea-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a03ea-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a03ea-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a03ea-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a03ea-108">DESCRIPTION</span></span>
<span data-ttu-id="a03ea-109">Il cmdlet **Get-AzSqlInstancePoolUsage** restituisce informazioni sull'utilizzo di un pool di istanze di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a03ea-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="a03ea-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a03ea-110">EXAMPLES</span></span>

### <span data-ttu-id="a03ea-111">Esempio 1: Ottiene l'utilizzo di un pool di istanze SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="a03ea-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
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

<span data-ttu-id="a03ea-112">Ottiene l'utilizzo per il pool di istanze SQL di Azure instancepool0.</span><span class="sxs-lookup"><span data-stu-id="a03ea-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="a03ea-113">Esempio 2: Ottiene l'utilizzo di un pool di istanze SQL di Azure usando un oggetto pool di istanze</span><span class="sxs-lookup"><span data-stu-id="a03ea-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
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

<span data-ttu-id="a03ea-114">Ottiene l'utilizzo per il pool di istanze SQL di Azure instancepool0 usando un oggetto pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="a03ea-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="a03ea-115">Esempio 3: Ottiene l'utilizzo di un pool di istanze SQL di Azure usando un ID risorsa di pool di istanze</span><span class="sxs-lookup"><span data-stu-id="a03ea-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
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

<span data-ttu-id="a03ea-116">Ottiene l'utilizzo per il pool di istanze SQL di Azure instancepool0 usando un identificatore di risorsa del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="a03ea-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="a03ea-117">Esempio 3: Ottiene l'utilizzo di un pool di istanze SQL di Azure con una ripartizione degli usi delle istanze gestite all'interno del pool.</span><span class="sxs-lookup"><span data-stu-id="a03ea-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
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

<span data-ttu-id="a03ea-118">Ottiene l'utilizzo per il pool di istanze SQL di Azure instancepool0 insieme agli usi delle istanze gestite in instancepool0.</span><span class="sxs-lookup"><span data-stu-id="a03ea-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="a03ea-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a03ea-119">PARAMETERS</span></span>

### <span data-ttu-id="a03ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a03ea-120">-DefaultProfile</span></span>
<span data-ttu-id="a03ea-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a03ea-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a03ea-122">-ExpandChildren</span><span class="sxs-lookup"><span data-stu-id="a03ea-122">-ExpandChildren</span></span>
<span data-ttu-id="a03ea-123">Flag che indica se espandere l'utilizzo di questo pool di istanze con l'utilizzo dei relativi elementi figlio.</span><span class="sxs-lookup"><span data-stu-id="a03ea-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

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

### <span data-ttu-id="a03ea-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="a03ea-124">-InstancePool</span></span>
<span data-ttu-id="a03ea-125">Oggetto pool di istanze padre.</span><span class="sxs-lookup"><span data-stu-id="a03ea-125">The parent instance pool object.</span></span>

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

### <span data-ttu-id="a03ea-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a03ea-126">-Name</span></span>
<span data-ttu-id="a03ea-127">Nome del pool di istanze gestito.</span><span class="sxs-lookup"><span data-stu-id="a03ea-127">The managed instance pool name.</span></span>

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

### <span data-ttu-id="a03ea-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a03ea-128">-ResourceGroupName</span></span>
<span data-ttu-id="a03ea-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a03ea-129">The resource group name.</span></span>

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

### <span data-ttu-id="a03ea-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a03ea-130">-ResourceId</span></span>
<span data-ttu-id="a03ea-131">ID risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="a03ea-131">The parent resource id.</span></span>

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

### <span data-ttu-id="a03ea-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a03ea-132">CommonParameters</span></span>
<span data-ttu-id="a03ea-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a03ea-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a03ea-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a03ea-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a03ea-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a03ea-135">INPUTS</span></span>

### <span data-ttu-id="a03ea-136">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="a03ea-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="a03ea-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a03ea-137">System.String</span></span>

## <span data-ttu-id="a03ea-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a03ea-138">OUTPUTS</span></span>

### <span data-ttu-id="a03ea-139">Microsoft. Azure. Commands. SQL. usages. Models. AzureSqlUsageModel</span><span class="sxs-lookup"><span data-stu-id="a03ea-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="a03ea-140">Note</span><span class="sxs-lookup"><span data-stu-id="a03ea-140">NOTES</span></span>

## <span data-ttu-id="a03ea-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a03ea-141">RELATED LINKS</span></span>
