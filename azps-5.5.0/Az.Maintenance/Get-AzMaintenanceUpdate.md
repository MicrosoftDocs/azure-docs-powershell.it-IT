---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207219"
---
# <span data-ttu-id="29a03-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="29a03-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="29a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29a03-102">SYNOPSIS</span></span>
<span data-ttu-id="29a03-103">Ottenere aggiornamenti di manutenzione in sospeso per le risorse.</span><span class="sxs-lookup"><span data-stu-id="29a03-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="29a03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29a03-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29a03-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="29a03-105">DESCRIPTION</span></span>
<span data-ttu-id="29a03-106">Ottenere aggiornamenti di manutenzione in sospeso per le risorse.</span><span class="sxs-lookup"><span data-stu-id="29a03-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="29a03-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29a03-107">EXAMPLES</span></span>

### <span data-ttu-id="29a03-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="29a03-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="29a03-109">Ottenere aggiornamenti di manutenzione in sospeso per le risorse.</span><span class="sxs-lookup"><span data-stu-id="29a03-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="29a03-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29a03-110">PARAMETERS</span></span>

### <span data-ttu-id="29a03-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29a03-111">-DefaultProfile</span></span>
<span data-ttu-id="29a03-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="29a03-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29a03-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="29a03-113">-ProviderName</span></span>
<span data-ttu-id="29a03-114">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="29a03-114">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a03-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29a03-115">-ResourceGroupName</span></span>
<span data-ttu-id="29a03-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="29a03-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a03-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="29a03-117">-ResourceName</span></span>
<span data-ttu-id="29a03-118">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="29a03-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a03-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="29a03-119">-ResourceParentName</span></span>
<span data-ttu-id="29a03-120">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="29a03-120">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a03-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="29a03-121">-ResourceParentType</span></span>
<span data-ttu-id="29a03-122">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="29a03-122">The parent resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a03-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="29a03-123">-ResourceType</span></span>
<span data-ttu-id="29a03-124">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="29a03-124">The resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29a03-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29a03-125">CommonParameters</span></span>
<span data-ttu-id="29a03-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29a03-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29a03-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="29a03-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29a03-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="29a03-128">INPUTS</span></span>

### <span data-ttu-id="29a03-129">System.String</span><span class="sxs-lookup"><span data-stu-id="29a03-129">System.String</span></span>

## <span data-ttu-id="29a03-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29a03-130">OUTPUTS</span></span>

### <span data-ttu-id="29a03-131">Microsoft.Azure.Management.Maintenance.Models.Update</span><span class="sxs-lookup"><span data-stu-id="29a03-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="29a03-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="29a03-132">NOTES</span></span>

## <span data-ttu-id="29a03-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29a03-133">RELATED LINKS</span></span>
