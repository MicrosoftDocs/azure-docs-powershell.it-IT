---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlInstance.md
ms.openlocfilehash: 72e3b740a84a46da094208b941e8b68173133e46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518515"
---
# <span data-ttu-id="eee5e-101">Get-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="eee5e-101">Get-AzureRmSqlInstance</span></span>

## <span data-ttu-id="eee5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eee5e-102">SYNOPSIS</span></span>
<span data-ttu-id="eee5e-103">Restituisce informazioni sull'istanza di database gestito di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="eee5e-103">Returns information about Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eee5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eee5e-104">SYNTAX</span></span>

### <span data-ttu-id="eee5e-105">GetInstanceByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eee5e-105">GetInstanceByResourceGroup (Default)</span></span>
```
Get-AzureRmSqlInstance [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eee5e-106">GetInstanceByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eee5e-106">GetInstanceByNameAndResourceGroup</span></span>
```
Get-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eee5e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eee5e-107">DESCRIPTION</span></span>
<span data-ttu-id="eee5e-108">Il cmdlet **Get-AzureRmSqlInstance** restituisce informazioni su una o più istanze gestite da SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="eee5e-108">The **Get-AzureRmSqlInstance** cmdlet returns information about one or more Azure SQL Managed Instances.</span></span>
<span data-ttu-id="eee5e-109">Specificare il nome di un'istanza per visualizzare le informazioni solo per quell'istanza.</span><span class="sxs-lookup"><span data-stu-id="eee5e-109">Specify the name of a instance to see information for only that instance.</span></span>

## <span data-ttu-id="eee5e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eee5e-110">EXAMPLES</span></span>

### <span data-ttu-id="eee5e-111">Esempio 1: ottenere tutte le istanze assegnate a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="eee5e-111">Example 1: Get all instances assigned to a resource group</span></span>
```
PS C:\>Get-AzureRmSqlInstance -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="eee5e-112">Questo comando consente di ottenere informazioni su tutte le istanze assegnate al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="eee5e-112">This command gets information about all instances assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="eee5e-113">Esempio 2: ottenere informazioni su un'istanza</span><span class="sxs-lookup"><span data-stu-id="eee5e-113">Example 2: Get information about an  instance</span></span>
```
PS C:\>Get-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
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

<span data-ttu-id="eee5e-114">Questo comando ottiene informazioni sull'istanza denominata managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="eee5e-114">This command gets information about the instance named managedInstance1.</span></span>

## <span data-ttu-id="eee5e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eee5e-115">PARAMETERS</span></span>

### <span data-ttu-id="eee5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eee5e-116">-DefaultProfile</span></span>
<span data-ttu-id="eee5e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eee5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee5e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="eee5e-118">-Name</span></span>
<span data-ttu-id="eee5e-119">Nome dell'istanza SQL.</span><span class="sxs-lookup"><span data-stu-id="eee5e-119">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee5e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eee5e-120">-ResourceGroupName</span></span>
<span data-ttu-id="eee5e-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eee5e-121">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetInstanceByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetInstanceByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eee5e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eee5e-122">CommonParameters</span></span>
<span data-ttu-id="eee5e-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eee5e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eee5e-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eee5e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eee5e-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eee5e-125">INPUTS</span></span>

### <span data-ttu-id="eee5e-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eee5e-126">None</span></span>

## <span data-ttu-id="eee5e-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eee5e-127">OUTPUTS</span></span>

### <span data-ttu-id="eee5e-128">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="eee5e-128">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="eee5e-129">Note</span><span class="sxs-lookup"><span data-stu-id="eee5e-129">NOTES</span></span>

## <span data-ttu-id="eee5e-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eee5e-130">RELATED LINKS</span></span>
