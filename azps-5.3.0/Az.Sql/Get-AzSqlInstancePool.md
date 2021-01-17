---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: afbd74953f876ede2a03e94c4db46937470a92dc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475642"
---
# <span data-ttu-id="67cfa-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="67cfa-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="67cfa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="67cfa-103">Restituisce informazioni sul pool di istanze di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="67cfa-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="67cfa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67cfa-104">SYNTAX</span></span>

### <span data-ttu-id="67cfa-105">ListBySubOrResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67cfa-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67cfa-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="67cfa-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67cfa-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="67cfa-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67cfa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67cfa-108">DESCRIPTION</span></span>
<span data-ttu-id="67cfa-109">Il cmdlet **Get-AzSqlInstancePool** restituisce informazioni su uno o più pool di istanze SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="67cfa-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="67cfa-110">Specificare il nome di un pool di istanze per visualizzare le informazioni solo per il pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="67cfa-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="67cfa-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67cfa-111">EXAMPLES</span></span>

### <span data-ttu-id="67cfa-112">Esempio 1: ottenere tutti i pool di istanze nell'abbonamento a un cliente</span><span class="sxs-lookup"><span data-stu-id="67cfa-112">Example 1: Get all instance pools across a customer subscription</span></span>
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

<span data-ttu-id="67cfa-113">Questo comando consente di ottenere informazioni su tutti i pool di istanze nell'abbonamento al cliente.</span><span class="sxs-lookup"><span data-stu-id="67cfa-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="67cfa-114">Esempio 2: ottenere tutti i pool di istanze in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="67cfa-114">Example 2: Get all instance pools across a resource group</span></span>
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

<span data-ttu-id="67cfa-115">Questo comando consente di ottenere informazioni su tutti i pool di istanze all'interno del gruppo di risorse resourcegroup01.</span><span class="sxs-lookup"><span data-stu-id="67cfa-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="67cfa-116">Esempio 3: ottenere informazioni su un pool di istanze</span><span class="sxs-lookup"><span data-stu-id="67cfa-116">Example 3: Get information about an instance pool</span></span>
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

<span data-ttu-id="67cfa-117">Questo comando consente di ottenere informazioni sul pool di istanze instancePool0.</span><span class="sxs-lookup"><span data-stu-id="67cfa-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="67cfa-118">Esempio 4: ottenere informazioni su un pool di istanze tramite ID risorsa pool di istanze</span><span class="sxs-lookup"><span data-stu-id="67cfa-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
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

<span data-ttu-id="67cfa-119">Questo comando ottiene le informazioni sul pool di istanze con il relativo identificatore di risorsa.</span><span class="sxs-lookup"><span data-stu-id="67cfa-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="67cfa-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67cfa-120">PARAMETERS</span></span>

### <span data-ttu-id="67cfa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67cfa-121">-DefaultProfile</span></span>
<span data-ttu-id="67cfa-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67cfa-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67cfa-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="67cfa-123">-Name</span></span>
<span data-ttu-id="67cfa-124">Nome del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="67cfa-124">The instance pool name.</span></span>

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

### <span data-ttu-id="67cfa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67cfa-125">-ResourceGroupName</span></span>
<span data-ttu-id="67cfa-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="67cfa-126">The resource group name.</span></span>

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

### <span data-ttu-id="67cfa-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67cfa-127">-ResourceId</span></span>
<span data-ttu-id="67cfa-128">Identificatore delle risorse del pool di istanze.</span><span class="sxs-lookup"><span data-stu-id="67cfa-128">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="67cfa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67cfa-129">CommonParameters</span></span>
<span data-ttu-id="67cfa-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67cfa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67cfa-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="67cfa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67cfa-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67cfa-132">INPUTS</span></span>

### <span data-ttu-id="67cfa-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="67cfa-133">None</span></span>

## <span data-ttu-id="67cfa-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67cfa-134">OUTPUTS</span></span>

### <span data-ttu-id="67cfa-135">Microsoft.Azure.Commands.Sql.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="67cfa-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="67cfa-136">Note</span><span class="sxs-lookup"><span data-stu-id="67cfa-136">NOTES</span></span>

## <span data-ttu-id="67cfa-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67cfa-137">RELATED LINKS</span></span>
