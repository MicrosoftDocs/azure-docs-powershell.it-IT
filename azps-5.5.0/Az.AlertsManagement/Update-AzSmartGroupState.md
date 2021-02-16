---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199775"
---
# <span data-ttu-id="7dfe2-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="7dfe2-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="7dfe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dfe2-102">SYNOPSIS</span></span>
<span data-ttu-id="7dfe2-103">Aggiorna lo stato smart del gruppo</span><span class="sxs-lookup"><span data-stu-id="7dfe2-103">Updates smart group state</span></span>

## <span data-ttu-id="7dfe2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7dfe2-104">SYNTAX</span></span>

### <span data-ttu-id="7dfe2-105">BySmartGroupId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7dfe2-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7dfe2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7dfe2-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7dfe2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7dfe2-107">DESCRIPTION</span></span>
<span data-ttu-id="7dfe2-108">Il cmdlet **Update-AzSmartGroupState** aggiorna lo stato smart group.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="7dfe2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7dfe2-109">EXAMPLES</span></span>

### <span data-ttu-id="7dfe2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7dfe2-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="7dfe2-111">Questo cmdlet aggiorna lo stato del gruppo smart ad Acknowleged.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="7dfe2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dfe2-112">PARAMETERS</span></span>

### <span data-ttu-id="7dfe2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dfe2-113">-DefaultProfile</span></span>
<span data-ttu-id="7dfe2-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7dfe2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7dfe2-115">-InputObject</span></span>
<span data-ttu-id="7dfe2-116">Oggetto di input dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7dfe2-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="7dfe2-117">-SmartGroupId</span></span>
<span data-ttu-id="7dfe2-118">Identificatore univoco di gruppo intelligente/ID risorsa del gruppo intelligente.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dfe2-119">-State</span><span class="sxs-lookup"><span data-stu-id="7dfe2-119">-State</span></span>
<span data-ttu-id="7dfe2-120">Stato del gruppo smart aggiornato</span><span class="sxs-lookup"><span data-stu-id="7dfe2-120">Updated Smart group State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dfe2-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7dfe2-121">-Confirm</span></span>
<span data-ttu-id="7dfe2-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dfe2-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dfe2-123">-WhatIf</span></span>
<span data-ttu-id="7dfe2-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7dfe2-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dfe2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dfe2-126">CommonParameters</span></span>
<span data-ttu-id="7dfe2-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dfe2-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7dfe2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dfe2-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="7dfe2-129">INPUTS</span></span>

### <span data-ttu-id="7dfe2-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7dfe2-130">None</span></span>

## <span data-ttu-id="7dfe2-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7dfe2-131">OUTPUTS</span></span>

### <span data-ttu-id="7dfe2-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="7dfe2-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="7dfe2-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="7dfe2-133">NOTES</span></span>

## <span data-ttu-id="7dfe2-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7dfe2-134">RELATED LINKS</span></span>
