---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: bd12fd2067c931f05266ed1ed24fb5666ead59a9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374681"
---
# <span data-ttu-id="50216-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="50216-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="50216-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50216-102">SYNOPSIS</span></span>
<span data-ttu-id="50216-103">Restituisce informazioni sul cluster virtuale di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="50216-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="50216-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50216-104">SYNTAX</span></span>

### <span data-ttu-id="50216-105">GetVirtualClusterByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50216-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50216-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50216-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50216-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="50216-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50216-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50216-108">DESCRIPTION</span></span>
<span data-ttu-id="50216-109">Il cmdlet **Get-AzSqlVirtualCluster** restituisce informazioni su uno o più cluster virtuali SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="50216-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="50216-110">Specificare il nome di un cluster virtuale per visualizzare le informazioni solo per il cluster.</span><span class="sxs-lookup"><span data-stu-id="50216-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="50216-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50216-111">EXAMPLES</span></span>

### <span data-ttu-id="50216-112">Esempio 1: ottenere tutti i cluster virtuali assegnati a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="50216-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
```powershell
PS C:> Get-AzSqlVirtualCluster -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster2
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster2
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name2

Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster3
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster3
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name3
```

<span data-ttu-id="50216-113">Questo comando consente di ottenere informazioni su tutti i cluster virtuali assegnati al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="50216-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="50216-114">Esempio 2: ottenere informazioni su un cluster virtuale specifico</span><span class="sxs-lookup"><span data-stu-id="50216-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="50216-115">Questo comando consente di ottenere informazioni sul cluster virtuale VirtualCluster1 nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="50216-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="50216-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50216-116">PARAMETERS</span></span>

### <span data-ttu-id="50216-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50216-117">-DefaultProfile</span></span>
<span data-ttu-id="50216-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50216-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50216-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="50216-119">-Name</span></span>
<span data-ttu-id="50216-120">Nome del cluster virtuale.</span><span class="sxs-lookup"><span data-stu-id="50216-120">The name of the virtual cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases: VirtualClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50216-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50216-121">-ResourceGroupName</span></span>
<span data-ttu-id="50216-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50216-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceGroup
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50216-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50216-123">-ResourceId</span></span>
<span data-ttu-id="50216-124">ID risorsa dell'oggetto Instance da ottenere</span><span class="sxs-lookup"><span data-stu-id="50216-124">The resource id of instance object to get</span></span>

```yaml
Type: System.String
Parameter Sets: GetVirtualClusterByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50216-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50216-125">CommonParameters</span></span>
<span data-ttu-id="50216-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50216-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50216-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50216-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50216-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50216-128">INPUTS</span></span>

### <span data-ttu-id="50216-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="50216-129">None</span></span>

## <span data-ttu-id="50216-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50216-130">OUTPUTS</span></span>

### <span data-ttu-id="50216-131">Microsoft. Azure. Commands. SQL. VirtualCluster. Model. AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="50216-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="50216-132">Note</span><span class="sxs-lookup"><span data-stu-id="50216-132">NOTES</span></span>

## <span data-ttu-id="50216-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50216-133">RELATED LINKS</span></span>
