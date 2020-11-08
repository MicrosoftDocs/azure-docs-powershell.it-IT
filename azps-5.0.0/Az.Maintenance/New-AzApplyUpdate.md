---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/new-azapplyupdate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/New-AzApplyUpdate.md
ms.openlocfilehash: 05403ce85b80238aeee8749322bdd94d28be68da
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201161"
---
# <span data-ttu-id="40475-101">New-AzApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="40475-101">New-AzApplyUpdate</span></span>

## <span data-ttu-id="40475-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40475-102">SYNOPSIS</span></span>
<span data-ttu-id="40475-103">Applicare gli aggiornamenti della manutenzione alla risorsa</span><span class="sxs-lookup"><span data-stu-id="40475-103">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="40475-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40475-104">SYNTAX</span></span>

```
New-AzApplyUpdate [-ResourceGroupName] <String> [-ProviderName] <String> [-ResourceParentType <String>]
 [-ResourceParentName <String>] [-ResourceType] <String> [-ResourceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40475-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40475-105">DESCRIPTION</span></span>
<span data-ttu-id="40475-106">Applicare gli aggiornamenti della manutenzione alla risorsa</span><span class="sxs-lookup"><span data-stu-id="40475-106">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="40475-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40475-107">EXAMPLES</span></span>

### <span data-ttu-id="40475-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40475-108">Example 1</span></span>
```powershell
PS C:\> New-AzApplyUpdate -ResourceGroupName smdtest$region -ResourceParentType hostGroups -ResourceParentName smddhg$region -ResourceType hosts -ResourceName smddh$region -ProviderName Microsoft.Compute


Status         : InProgress
ResourceId     : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2
LastUpdateTime : 11/8/2019 9:39:01 AM
Id             :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/applyUpdates/cbd4c97d-2011-4fa3-9df1-525f97e74eac
Name           : cbd4c97d-2011-4fa3-9df1-525f97e74eac
Type           : Microsoft.Maintenance/applyUpdates
```

<span data-ttu-id="40475-109">Applicare gli aggiornamenti della manutenzione alla risorsa</span><span class="sxs-lookup"><span data-stu-id="40475-109">Apply maintenance updates to resource</span></span>

## <span data-ttu-id="40475-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40475-110">PARAMETERS</span></span>

### <span data-ttu-id="40475-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="40475-111">-AsJob</span></span>
<span data-ttu-id="40475-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="40475-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40475-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40475-113">-DefaultProfile</span></span>
<span data-ttu-id="40475-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40475-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40475-115">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="40475-115">-ProviderName</span></span>
<span data-ttu-id="40475-116">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="40475-116">The resource provider Name.</span></span>

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

### <span data-ttu-id="40475-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40475-117">-ResourceGroupName</span></span>
<span data-ttu-id="40475-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40475-118">The resource Group Name.</span></span>

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

### <span data-ttu-id="40475-119">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="40475-119">-ResourceName</span></span>
<span data-ttu-id="40475-120">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="40475-120">The resource name.</span></span>

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

### <span data-ttu-id="40475-121">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="40475-121">-ResourceParentName</span></span>
<span data-ttu-id="40475-122">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="40475-122">The parent resource name.</span></span>

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

### <span data-ttu-id="40475-123">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="40475-123">-ResourceParentType</span></span>
<span data-ttu-id="40475-124">Tipo di risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="40475-124">The parent resource type.</span></span>

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

### <span data-ttu-id="40475-125">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="40475-125">-ResourceType</span></span>
<span data-ttu-id="40475-126">Tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="40475-126">The resource type.</span></span>

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

### <span data-ttu-id="40475-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="40475-127">-Confirm</span></span>
<span data-ttu-id="40475-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40475-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40475-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40475-129">-WhatIf</span></span>
<span data-ttu-id="40475-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40475-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40475-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="40475-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40475-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40475-132">CommonParameters</span></span>
<span data-ttu-id="40475-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40475-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40475-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="40475-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40475-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40475-135">INPUTS</span></span>

### <span data-ttu-id="40475-136">System. String</span><span class="sxs-lookup"><span data-stu-id="40475-136">System.String</span></span>

## <span data-ttu-id="40475-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40475-137">OUTPUTS</span></span>

### <span data-ttu-id="40475-138">Microsoft. Azure. Commands. Maintenance. Models. PSApplyUpdate</span><span class="sxs-lookup"><span data-stu-id="40475-138">Microsoft.Azure.Commands.Maintenance.Models.PSApplyUpdate</span></span>

## <span data-ttu-id="40475-139">Note</span><span class="sxs-lookup"><span data-stu-id="40475-139">NOTES</span></span>

## <span data-ttu-id="40475-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40475-140">RELATED LINKS</span></span>
