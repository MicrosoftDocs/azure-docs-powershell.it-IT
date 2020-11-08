---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceUpdate.md
ms.openlocfilehash: d8d3e4df3349acb1340a24362043d32d528fc284
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022181"
---
# <span data-ttu-id="4dd27-101">Get-AzMaintenanceUpdate</span><span class="sxs-lookup"><span data-stu-id="4dd27-101">Get-AzMaintenanceUpdate</span></span>

## <span data-ttu-id="4dd27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4dd27-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd27-103">Ottenere gli aggiornamenti della manutenzione in sospeso per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="4dd27-103">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="4dd27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dd27-104">SYNTAX</span></span>

```
Get-AzMaintenanceUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dd27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dd27-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd27-106">Ottenere gli aggiornamenti della manutenzione in sospeso per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="4dd27-106">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="4dd27-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dd27-107">EXAMPLES</span></span>

### <span data-ttu-id="4dd27-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4dd27-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceUpdate -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute

MaintenanceScope    : Host
ImpactType          : Freeze
Status              : Pending
ImpactDurationInSec : 9
NotBefore           : 1/24/2020 5:11:41 AM
ResourceId          : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
```

<span data-ttu-id="4dd27-109">Ottenere gli aggiornamenti della manutenzione in sospeso per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="4dd27-109">Get pending maintenance updates to resource.</span></span>

## <span data-ttu-id="4dd27-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4dd27-110">PARAMETERS</span></span>

### <span data-ttu-id="4dd27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd27-111">-DefaultProfile</span></span>
<span data-ttu-id="4dd27-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd27-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd27-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="4dd27-113">-ProviderName</span></span>
<span data-ttu-id="4dd27-114">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="4dd27-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="4dd27-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dd27-115">-ResourceGroupName</span></span>
<span data-ttu-id="4dd27-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4dd27-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="4dd27-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4dd27-117">-ResourceName</span></span>
<span data-ttu-id="4dd27-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4dd27-118">The resource name.</span></span>

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

### <span data-ttu-id="4dd27-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="4dd27-119">-ResourceParentName</span></span>
<span data-ttu-id="4dd27-120">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="4dd27-120">The parent resource name.</span></span>

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

### <span data-ttu-id="4dd27-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="4dd27-121">-ResourceParentType</span></span>
<span data-ttu-id="4dd27-122">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="4dd27-122">The parent resource type.</span></span>

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

### <span data-ttu-id="4dd27-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="4dd27-123">-ResourceType</span></span>
<span data-ttu-id="4dd27-124">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="4dd27-124">The resource type.</span></span>

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

### <span data-ttu-id="4dd27-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd27-125">CommonParameters</span></span>
<span data-ttu-id="4dd27-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd27-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd27-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dd27-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd27-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4dd27-128">INPUTS</span></span>

### <span data-ttu-id="4dd27-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4dd27-129">System.String</span></span>

## <span data-ttu-id="4dd27-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dd27-130">OUTPUTS</span></span>

### <span data-ttu-id="4dd27-131">Microsoft. Azure. Management. Maintenance. Models. Update</span><span class="sxs-lookup"><span data-stu-id="4dd27-131">Microsoft.Azure.Management.Maintenance.Models.Update</span></span>

## <span data-ttu-id="4dd27-132">Note</span><span class="sxs-lookup"><span data-stu-id="4dd27-132">NOTES</span></span>

## <span data-ttu-id="4dd27-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dd27-133">RELATED LINKS</span></span>
