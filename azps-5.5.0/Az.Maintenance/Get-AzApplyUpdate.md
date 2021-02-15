---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzApplyUpdate.md
ms.openlocfilehash: 35f504731ae176af9d476e770bc243c394ceb7af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207251"
---
# <span data-ttu-id="6ca80-101">Get-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="6ca80-101">Get-AzApplyUpdate</span></span>

## <span data-ttu-id="6ca80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ca80-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca80-103">Tenere traccia degli aggiornamenti di manutenzione delle risorse</span><span class="sxs-lookup"><span data-stu-id="6ca80-103">Track maintenance updates to resource</span></span>

## <span data-ttu-id="6ca80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ca80-104">SYNTAX</span></span>

```
Get-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> -ApplyUpdateName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ca80-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6ca80-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca80-106">Tenere traccia degli aggiornamenti di manutenzione delle risorse</span><span class="sxs-lookup"><span data-stu-id="6ca80-106">Track maintenance updates to resource</span></span>

## <span data-ttu-id="6ca80-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ca80-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca80-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ca80-108">Example 1</span></span>
```powershell
PS C:\> Get-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute -ApplyUpdateName default


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/default
Name           : default
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="6ca80-109">Tenere traccia degli aggiornamenti di manutenzione delle risorse</span><span class="sxs-lookup"><span data-stu-id="6ca80-109">Track maintenance updates to resource</span></span>

## <span data-ttu-id="6ca80-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ca80-110">PARAMETERS</span></span>

### <span data-ttu-id="6ca80-111">-ApplyUpdateName</span><span class="sxs-lookup"><span data-stu-id="6ca80-111">-ApplyUpdateName</span></span>
<span data-ttu-id="6ca80-112">Nome della risorsa di aggiornamento applicabile.</span><span class="sxs-lookup"><span data-stu-id="6ca80-112">The apply update resource name.</span></span>

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

### <span data-ttu-id="6ca80-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca80-113">-DefaultProfile</span></span>
<span data-ttu-id="6ca80-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ca80-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ca80-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="6ca80-115">-ProviderName</span></span>
<span data-ttu-id="6ca80-116">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ca80-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="6ca80-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca80-117">-ResourceGroupName</span></span>
<span data-ttu-id="6ca80-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ca80-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="6ca80-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6ca80-119">-ResourceName</span></span>
<span data-ttu-id="6ca80-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ca80-120">The resource name.</span></span>

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

### <span data-ttu-id="6ca80-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="6ca80-121">-ResourceParentName</span></span>
<span data-ttu-id="6ca80-122">Nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="6ca80-122">The parent resource name.</span></span>

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

### <span data-ttu-id="6ca80-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="6ca80-123">-ResourceParentType</span></span>
<span data-ttu-id="6ca80-124">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="6ca80-124">The parent resource type.</span></span>

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

### <span data-ttu-id="6ca80-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6ca80-125">-ResourceType</span></span>
<span data-ttu-id="6ca80-126">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6ca80-126">The resource type.</span></span>

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

### <span data-ttu-id="6ca80-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca80-127">CommonParameters</span></span>
<span data-ttu-id="6ca80-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca80-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca80-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ca80-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca80-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="6ca80-130">INPUTS</span></span>

### <span data-ttu-id="6ca80-131">System.String</span><span class="sxs-lookup"><span data-stu-id="6ca80-131">System.String</span></span>

## <span data-ttu-id="6ca80-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ca80-132">OUTPUTS</span></span>

### <span data-ttu-id="6ca80-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="6ca80-133">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="6ca80-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="6ca80-134">NOTES</span></span>

## <span data-ttu-id="6ca80-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ca80-135">RELATED LINKS</span></span>
