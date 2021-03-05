---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlvirtualcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlVirtualCluster.md
ms.openlocfilehash: 624ca943d9adf7df105fae18a0a4a8ccad2b9b9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984061"
---
# <span data-ttu-id="f48e2-101">Get-AzSqlVirtualCluster</span><span class="sxs-lookup"><span data-stu-id="f48e2-101">Get-AzSqlVirtualCluster</span></span>

## <span data-ttu-id="f48e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f48e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f48e2-103">Restituisce informazioni su Azure SQL cluster virtuale.</span><span class="sxs-lookup"><span data-stu-id="f48e2-103">Returns information about Azure SQL Virtual Cluster.</span></span>

## <span data-ttu-id="f48e2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f48e2-104">SYNTAX</span></span>

### <span data-ttu-id="f48e2-105">GetVirtualClusterByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f48e2-105">GetVirtualClusterByResourceGroup (Default)</span></span>
```
Get-AzSqlVirtualCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f48e2-106">GetVirtualClusterByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f48e2-106">GetVirtualClusterByNameAndResourceGroup</span></span>
```
Get-AzSqlVirtualCluster [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f48e2-107">GetVirtualClusterByResourceId</span><span class="sxs-lookup"><span data-stu-id="f48e2-107">GetVirtualClusterByResourceId</span></span>
```
Get-AzSqlVirtualCluster [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f48e2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f48e2-108">DESCRIPTION</span></span>
<span data-ttu-id="f48e2-109">Il cmdlet **Get-AzSqlVirtualCluster** restituisce informazioni su uno o più cluster virtuali SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f48e2-109">The **Get-AzSqlVirtualCluster** cmdlet returns information about one or more Azure SQL Virtual Clusters.</span></span>
<span data-ttu-id="f48e2-110">Specificare il nome di un cluster virtuale per visualizzare informazioni solo per quel cluster.</span><span class="sxs-lookup"><span data-stu-id="f48e2-110">Specify the name of a virtual cluster to see information for only that cluster.</span></span>

## <span data-ttu-id="f48e2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f48e2-111">EXAMPLES</span></span>

### <span data-ttu-id="f48e2-112">Esempio 1: Assegnare tutti i cluster virtuali a un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f48e2-112">Example 1: Get all virtual clusters assigned to a resource group</span></span>
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

<span data-ttu-id="f48e2-113">Questo comando recupera informazioni su tutti i cluster virtuali assegnati al gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f48e2-113">This command gets information about all Virtual Clusters assigned to the resource group ResourceGroup01.</span></span>

### <span data-ttu-id="f48e2-114">Esempio 2: Ottenere informazioni su un cluster virtuale specifico</span><span class="sxs-lookup"><span data-stu-id="f48e2-114">Example 2: Get information about specific virtual cluster</span></span>
```
PS C:\>  Get-AzSqlVirtualCluster -Name VirtualCluster1 -ResourceGroupName ResourceGroup01


Location           : eastus
Id                 : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/virtualClusters/VirtualCluster1
ResourceGroupName  : ResourceGroup01
VirtualClusterName : VirtualCluster1
Tags               :
SubnetId           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name1
```

<span data-ttu-id="f48e2-115">Questo comando ottiene informazioni sul cluster virtuale VirtualCluster1 nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f48e2-115">This command gets information about the virtual cluster VirtualCluster1 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f48e2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f48e2-116">PARAMETERS</span></span>

### <span data-ttu-id="f48e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f48e2-117">-DefaultProfile</span></span>
<span data-ttu-id="f48e2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f48e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f48e2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f48e2-119">-Name</span></span>
<span data-ttu-id="f48e2-120">Nome del cluster virtuale.</span><span class="sxs-lookup"><span data-stu-id="f48e2-120">The name of the virtual cluster.</span></span>

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

### <span data-ttu-id="f48e2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f48e2-121">-ResourceGroupName</span></span>
<span data-ttu-id="f48e2-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f48e2-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="f48e2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f48e2-123">-ResourceId</span></span>
<span data-ttu-id="f48e2-124">ID risorsa dell'oggetto istanza da ottenere</span><span class="sxs-lookup"><span data-stu-id="f48e2-124">The resource id of instance object to get</span></span>

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

### <span data-ttu-id="f48e2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f48e2-125">CommonParameters</span></span>
<span data-ttu-id="f48e2-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f48e2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f48e2-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f48e2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f48e2-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="f48e2-128">INPUTS</span></span>

### <span data-ttu-id="f48e2-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f48e2-129">None</span></span>

## <span data-ttu-id="f48e2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f48e2-130">OUTPUTS</span></span>

### <span data-ttu-id="f48e2-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span><span class="sxs-lookup"><span data-stu-id="f48e2-131">Microsoft.Azure.Commands.Sql.VirtualCluster.Model.AzureSqlVirtualClusterModel</span></span>

## <span data-ttu-id="f48e2-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="f48e2-132">NOTES</span></span>

## <span data-ttu-id="f48e2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f48e2-133">RELATED LINKS</span></span>
