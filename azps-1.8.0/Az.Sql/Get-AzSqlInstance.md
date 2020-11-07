---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstance.md
ms.openlocfilehash: a21b2436f44cb2df5f9984e70ccecf6c1d9c306a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676937"
---
# <span data-ttu-id="089b9-101">Get-AzSqlInstance</span><span class="sxs-lookup"><span data-stu-id="089b9-101">Get-AzSqlInstance</span></span>

## <span data-ttu-id="089b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="089b9-102">SYNOPSIS</span></span>
<span data-ttu-id="089b9-103">Restituisce informazioni sull'istanza di database gestito di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="089b9-103">Returns information about Azure SQL Managed Database Instance.</span></span>

## <span data-ttu-id="089b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="089b9-104">SYNTAX</span></span>

```
Get-AzSqlInstance [[-Name] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="089b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="089b9-105">DESCRIPTION</span></span>
<span data-ttu-id="089b9-106">Il cmdlet **Get-AzSqlInstance** restituisce informazioni su una o più istanze gestite da SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="089b9-106">The **Get-AzSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="089b9-107">Specificare il nome di un'istanza per visualizzare le informazioni solo per quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="089b9-107">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="089b9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="089b9-108">EXAMPLES</span></span>

### <span data-ttu-id="089b9-109">Esempio 1: ottenere tutte le istanze assegnate a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="089b9-109">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="089b9-110">Questo comando consente di ottenere informazioni su tutte le istanze assegnate al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="089b9-110">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="089b9-111">Esempio 2: ottenere informazioni su un'istanza</span><span class="sxs-lookup"><span data-stu-id="089b9-111">Example 2: Get information about an  instance</span></span>
```
PS C:\> Get-AzSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="089b9-112">Questo comando ottiene informazioni sull'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="089b9-112">This command gets information about the instance named managedInstance1.</span></span>

### <span data-ttu-id="089b9-113">Esempio 3: ottenere tutte le istanze assegnate a un gruppo di risorse tramite il filtro</span><span class="sxs-lookup"><span data-stu-id="089b9-113">Example 3: Get all instances assigned to a resource group using filtering</span></span>
```
PS C:\> Get-AzSqlInstance -ResourceGroupName "ResourceGroup01" -Name "managedInstance*"
Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance1
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance1
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance1.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin1
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512

Location                 : westcentralus
Id                       : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/managedInstances/managedInstance2
ResourceGroupName        : resourcegroup01
ManagedInstanceName      : managedInstance2
Tags                     :
Identity                 : Microsoft.Azure.Management.Sql.Models.ResourceIdentity
Sku                      : Microsoft.Azure.Management.Internal.Resources.Models.Sku
FullyQualifiedDomainName : managedInstance2.wcusxxxxxxxxxxxxx.database.windows.net
AdministratorLogin       : adminLogin2
AdministratorPassword    :
SubnetId                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
LicenseType              : BasePrice
VCores                   : 8
StorageSizeInGB          : 512
```

<span data-ttu-id="089b9-114">Questo comando consente di ottenere informazioni su tutte le istanze assegnate al gruppo di risorse ResourceGroup01 che iniziano con "managedInstance".</span><span class="sxs-lookup"><span data-stu-id="089b9-114">This command gets information about all instances assigned to the resource group ResourceGroup01 that start with "managedInstance".</span></span>

## <span data-ttu-id="089b9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="089b9-115">PARAMETERS</span></span>

### <span data-ttu-id="089b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089b9-116">-DefaultProfile</span></span>
<span data-ttu-id="089b9-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="089b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="089b9-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="089b9-118">-Name</span></span>
<span data-ttu-id="089b9-119">Nome dell'istanza SQL.</span><span class="sxs-lookup"><span data-stu-id="089b9-119">SQL instance name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="089b9-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="089b9-120">-ResourceGroupName</span></span>
<span data-ttu-id="089b9-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="089b9-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="089b9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089b9-122">CommonParameters</span></span>
<span data-ttu-id="089b9-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="089b9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089b9-124">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="089b9-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089b9-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="089b9-125">INPUTS</span></span>

### <span data-ttu-id="089b9-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="089b9-126">None</span></span>

## <span data-ttu-id="089b9-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="089b9-127">OUTPUTS</span></span>

### <span data-ttu-id="089b9-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="089b9-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="089b9-129">Note</span><span class="sxs-lookup"><span data-stu-id="089b9-129">NOTES</span></span>

## <span data-ttu-id="089b9-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="089b9-130">RELATED LINKS</span></span>
