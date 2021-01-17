---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475955"
---
# <span data-ttu-id="f842b-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="f842b-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="f842b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f842b-102">SYNOPSIS</span></span>
<span data-ttu-id="f842b-103">Aggiorna lo stato del gruppo smart</span><span class="sxs-lookup"><span data-stu-id="f842b-103">Updates smart group state</span></span>

## <span data-ttu-id="f842b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f842b-104">SYNTAX</span></span>

### <span data-ttu-id="f842b-105">BySmartGroupId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f842b-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f842b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f842b-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f842b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f842b-107">DESCRIPTION</span></span>
<span data-ttu-id="f842b-108">**Update-AzSmartGroupState** cmdlet aggiorna lo stato dello Smart Group.</span><span class="sxs-lookup"><span data-stu-id="f842b-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="f842b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f842b-109">EXAMPLES</span></span>

### <span data-ttu-id="f842b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f842b-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="f842b-111">Questo cmdlet aggiorna lo stato del gruppo smart in acknowleged.</span><span class="sxs-lookup"><span data-stu-id="f842b-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="f842b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f842b-112">PARAMETERS</span></span>

### <span data-ttu-id="f842b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f842b-113">-DefaultProfile</span></span>
<span data-ttu-id="f842b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f842b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f842b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f842b-115">-InputObject</span></span>
<span data-ttu-id="f842b-116">Oggetto di input da pipeline.</span><span class="sxs-lookup"><span data-stu-id="f842b-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="f842b-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="f842b-117">-SmartGroupId</span></span>
<span data-ttu-id="f842b-118">Identificatore univoco di Smart Group/ResourceId di Smart Group.</span><span class="sxs-lookup"><span data-stu-id="f842b-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="f842b-119">-Stato</span><span class="sxs-lookup"><span data-stu-id="f842b-119">-State</span></span>
<span data-ttu-id="f842b-120">Stato Smart Group aggiornato</span><span class="sxs-lookup"><span data-stu-id="f842b-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="f842b-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f842b-121">-Confirm</span></span>
<span data-ttu-id="f842b-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f842b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f842b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f842b-123">-WhatIf</span></span>
<span data-ttu-id="f842b-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f842b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f842b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f842b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f842b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f842b-126">CommonParameters</span></span>
<span data-ttu-id="f842b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f842b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f842b-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f842b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f842b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f842b-129">INPUTS</span></span>

### <span data-ttu-id="f842b-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f842b-130">None</span></span>

## <span data-ttu-id="f842b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f842b-131">OUTPUTS</span></span>

### <span data-ttu-id="f842b-132">Microsoft. Azure. Commands. AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="f842b-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="f842b-133">Note</span><span class="sxs-lookup"><span data-stu-id="f842b-133">NOTES</span></span>

## <span data-ttu-id="f842b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f842b-134">RELATED LINKS</span></span>
