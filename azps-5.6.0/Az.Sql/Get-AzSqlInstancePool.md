---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: 524d9ff479355f511b9039e1ea64a8234e37e021
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999325"
---
# <span data-ttu-id="ad13e-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="ad13e-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="ad13e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad13e-102">SYNOPSIS</span></span>
<span data-ttu-id="ad13e-103">Restituisce informazioni sul pool di istanze SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ad13e-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="ad13e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ad13e-104">SYNTAX</span></span>

### <span data-ttu-id="ad13e-105">ListBySubOrResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ad13e-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad13e-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad13e-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad13e-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad13e-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad13e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ad13e-108">DESCRIPTION</span></span>
<span data-ttu-id="ad13e-109">Il cmdlet **Get-AzSqlInstancePool** restituisce informazioni su uno o più pool di istanze SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ad13e-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="ad13e-110">Specificare il nome di un pool di istanze per visualizzare informazioni solo per tale pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ad13e-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="ad13e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ad13e-111">EXAMPLES</span></span>

### <span data-ttu-id="ad13e-112">Esempio 1: Ottenere tutti i pool di istanze nell'abbonamento di un cliente</span><span class="sxs-lookup"><span data-stu-id="ad13e-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
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

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="ad13e-113">Questo comando ottiene informazioni su tutti i pool di istanze all'interno della sottoscrizione del cliente.</span><span class="sxs-lookup"><span data-stu-id="ad13e-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="ad13e-114">Esempio 2: Ottenere tutti i pool di istanze in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ad13e-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
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

<span data-ttu-id="ad13e-115">Questo comando ottiene informazioni su tutti i pool di istanze all'interno del gruppo di risorse resourcegroup01.</span><span class="sxs-lookup"><span data-stu-id="ad13e-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="ad13e-116">Esempio 3: Ottenere informazioni su un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="ad13e-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
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

<span data-ttu-id="ad13e-117">Questo comando recupera informazioni sull'istanza pool di istanze Pool0.</span><span class="sxs-lookup"><span data-stu-id="ad13e-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="ad13e-118">Esempio 4: Ottenere informazioni su un pool di istanze usando l'ID risorsa pool di istanze</span><span class="sxs-lookup"><span data-stu-id="ad13e-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
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

<span data-ttu-id="ad13e-119">Questo comando ottiene informazioni sul pool di istanze con il relativo identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="ad13e-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="ad13e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad13e-120">PARAMETERS</span></span>

### <span data-ttu-id="ad13e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad13e-121">-DefaultProfile</span></span>
<span data-ttu-id="ad13e-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad13e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad13e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ad13e-123">-Name</span></span>
<span data-ttu-id="ad13e-124">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ad13e-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad13e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad13e-125">-ResourceGroupName</span></span>
<span data-ttu-id="ad13e-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ad13e-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad13e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad13e-127">-ResourceId</span></span>
<span data-ttu-id="ad13e-128">L'identificatore di risorsa del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="ad13e-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad13e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad13e-129">CommonParameters</span></span>
<span data-ttu-id="ad13e-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad13e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad13e-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ad13e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad13e-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="ad13e-132">INPUTS</span></span>

### <span data-ttu-id="ad13e-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ad13e-133">None</span></span>

## <span data-ttu-id="ad13e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ad13e-134">OUTPUTS</span></span>

### <span data-ttu-id="ad13e-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="ad13e-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="ad13e-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="ad13e-136">NOTES</span></span>

## <span data-ttu-id="ad13e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ad13e-137">RELATED LINKS</span></span>
