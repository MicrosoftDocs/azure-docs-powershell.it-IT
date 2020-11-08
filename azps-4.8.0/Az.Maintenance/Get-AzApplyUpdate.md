---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189615"
---
# <span data-ttu-id="9d206-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="9d206-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="9d206-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d206-102">SYNOPSIS</span></span>
<span data-ttu-id="9d206-103">Tenere traccia degli aggiornamenti della manutenzione alla risorsa</span><span class="sxs-lookup"><span data-stu-id="9d206-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="9d206-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d206-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d206-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d206-105">DESCRIPTION</span></span>
<span data-ttu-id="9d206-106">Tenere traccia degli aggiornamenti della manutenzione alla risorsa</span><span class="sxs-lookup"><span data-stu-id="9d206-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="9d206-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d206-107">EXAMPLES</span></span>

### <span data-ttu-id="9d206-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9d206-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="9d206-109">Tenere traccia degli aggiornamenti della manutenzione alla risorsa</span><span class="sxs-lookup"><span data-stu-id="9d206-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="9d206-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d206-110">PARAMETERS</span></span>

### <span data-ttu-id="9d206-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="9d206-111">-ApplyUpdateName</span></span>
<span data-ttu-id="9d206-112">Il nome della risorsa applica aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="9d206-112">The apply update resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d206-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d206-113">-DefaultProfile</span></span>
<span data-ttu-id="9d206-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d206-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d206-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="9d206-115">-ProviderName</span></span>
<span data-ttu-id="9d206-116">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d206-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="9d206-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d206-117">-ResourceGroupName</span></span>
<span data-ttu-id="9d206-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d206-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="9d206-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9d206-119">-ResourceName</span></span>
<span data-ttu-id="9d206-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9d206-120">The resource name.</span></span>

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

### <span data-ttu-id="9d206-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="9d206-121">-ResourceParentName</span></span>
<span data-ttu-id="9d206-122">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="9d206-122">The parent resource name.</span></span>

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

### <span data-ttu-id="9d206-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="9d206-123">-ResourceParentType</span></span>
<span data-ttu-id="9d206-124">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="9d206-124">The parent resource type.</span></span>

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

### <span data-ttu-id="9d206-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9d206-125">-ResourceType</span></span>
<span data-ttu-id="9d206-126">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="9d206-126">The resource type.</span></span>

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

### <span data-ttu-id="9d206-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d206-127">CommonParameters</span></span>
<span data-ttu-id="9d206-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d206-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d206-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d206-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d206-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d206-130">INPUTS</span></span>

### <span data-ttu-id="9d206-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9d206-131">System.String</span></span>

## <span data-ttu-id="9d206-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d206-132">OUTPUTS</span></span>

### <span data-ttu-id="9d206-133">Microsoft. Azure. Commands. Maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="9d206-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="9d206-134">Note</span><span class="sxs-lookup"><span data-stu-id="9d206-134">NOTES</span></span>

## <span data-ttu-id="9d206-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d206-135">RELATED LINKS</span></span>