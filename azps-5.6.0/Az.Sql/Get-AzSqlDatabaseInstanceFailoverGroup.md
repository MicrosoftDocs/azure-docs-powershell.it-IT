---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 2b8ddc8b15ca9fa7322de231f9688548c4073708
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014781"
---
# <span data-ttu-id="dbae6-101">Get-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="dbae6-101">Get-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="dbae6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbae6-102">SYNOPSIS</span></span>
<span data-ttu-id="dbae6-103">Ottiene o elenca i gruppi di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="dbae6-103">Gets or lists Instance Failover Groups.</span></span>

## <span data-ttu-id="dbae6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbae6-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseInstanceFailoverGroup [[-Name] <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbae6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dbae6-105">DESCRIPTION</span></span>
<span data-ttu-id="dbae6-106">Recupera un gruppo di failover dell'istanza specifico o elenca i gruppi di failover delle istanze in un'area nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="dbae6-106">Gets a specific Instance Failover Group or lists the Instance Failover Groups in a region under the user's subscription.</span></span>

<span data-ttu-id="dbae6-107">Per eseguire il comando è possibile usare entrambe le aree del gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="dbae6-107">Either region in the Instance Failover Group may be used to execute the command.</span></span> <span data-ttu-id="dbae6-108">I valori restituiti rifletteranno lo stato delle istanze gestite in tale area rispetto al gruppo di failover delle istanze.</span><span class="sxs-lookup"><span data-stu-id="dbae6-108">The returned values will reflect the state of the Managed Instances in that region with respect to the Instance Failover Group.</span></span>

## <span data-ttu-id="dbae6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbae6-109">EXAMPLES</span></span>

### <span data-ttu-id="dbae6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dbae6-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location
Output:
{
    ResourceGroupName                     : rg
    Location                              : East US
    Name                                  : fg
    PartnerResourceGroupName              : rg
    PartnerRegion                         : West US
    PrimaryManagedInstanceName            : managedInstance1
    PartnerManagedInstanceName            : managedInstance2
    ReplicationRole                       : Primary
    ReplicationState                      : CATCH_UP
    ReadWriteFailoverPolicy               : Automatic
    FailoverWithDataLossGracePeriodHours  : 1
    ReadOnlyFailoverPolicy                : Disabled
    Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
}
```

<span data-ttu-id="dbae6-111">Elenca tutti i gruppi di failover nell'area geografica</span><span class="sxs-lookup"><span data-stu-id="dbae6-111">Lists all Failover Groups in the region</span></span>

### <span data-ttu-id="dbae6-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="dbae6-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="dbae6-113">Ottenere un gruppo di failover dell'istanza specifico.</span><span class="sxs-lookup"><span data-stu-id="dbae6-113">Get a specific Instance Failover Group.</span></span>

## <span data-ttu-id="dbae6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbae6-114">PARAMETERS</span></span>

### <span data-ttu-id="dbae6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbae6-115">-DefaultProfile</span></span>
<span data-ttu-id="dbae6-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbae6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbae6-117">-Location</span><span class="sxs-lookup"><span data-stu-id="dbae6-117">-Location</span></span>
<span data-ttu-id="dbae6-118">Nome dell'area locale da cui recuperare il gruppo di failover dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="dbae6-118">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbae6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="dbae6-119">-Name</span></span>
<span data-ttu-id="dbae6-120">Nome del gruppo di failover dell'istanza da recuperare.</span><span class="sxs-lookup"><span data-stu-id="dbae6-120">The name of the Instance Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbae6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbae6-121">-ResourceGroupName</span></span>
<span data-ttu-id="dbae6-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbae6-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbae6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbae6-123">CommonParameters</span></span>
<span data-ttu-id="dbae6-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbae6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbae6-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dbae6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbae6-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="dbae6-126">INPUTS</span></span>

### <span data-ttu-id="dbae6-127">System.String</span><span class="sxs-lookup"><span data-stu-id="dbae6-127">System.String</span></span>

## <span data-ttu-id="dbae6-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbae6-128">OUTPUTS</span></span>

### <span data-ttu-id="dbae6-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="dbae6-129">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="dbae6-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="dbae6-130">NOTES</span></span>

## <span data-ttu-id="dbae6-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbae6-131">RELATED LINKS</span></span>
