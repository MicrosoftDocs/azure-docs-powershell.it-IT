---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018765"
---
# <span data-ttu-id="75f0b-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="75f0b-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="75f0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="75f0b-102">SYNOPSIS</span></span>
<span data-ttu-id="75f0b-103">Aggiornare il mapping del contenitore di protezione del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="75f0b-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="75f0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="75f0b-104">SYNTAX</span></span>

### <span data-ttu-id="75f0b-105">AzureToAzureEnableAutoUpdate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="75f0b-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75f0b-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="75f0b-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75f0b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="75f0b-107">DESCRIPTION</span></span>
<span data-ttu-id="75f0b-108">Il cmdlet **Update-AzRecoveryServicesAsrProtectionContainerMapping** aggiorna il mapping del contenitore di protezione del ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="75f0b-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="75f0b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="75f0b-109">EXAMPLES</span></span>

### <span data-ttu-id="75f0b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="75f0b-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="75f0b-111">Avviare l'operazione per disabilitare l'aggiornamento automatico per container.</span><span class="sxs-lookup"><span data-stu-id="75f0b-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="75f0b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="75f0b-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="75f0b-113">Avviare l'operazione per disabilitare Enable Auto Update per container.</span><span class="sxs-lookup"><span data-stu-id="75f0b-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="75f0b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="75f0b-114">PARAMETERS</span></span>

### <span data-ttu-id="75f0b-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="75f0b-115">-AutomationAccountId</span></span>
<span data-ttu-id="75f0b-116">Specifica il accountId di automazione usato per la UDPATE automatica.</span><span class="sxs-lookup"><span data-stu-id="75f0b-116">Specifies the automation accountId used for auto udpate.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f0b-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="75f0b-117">-AzureToAzure</span></span>
<span data-ttu-id="75f0b-118">Specifica Azure to Azure Protection container.</span><span class="sxs-lookup"><span data-stu-id="75f0b-118">Specifies Azure to Azure protection container.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f0b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75f0b-119">-DefaultProfile</span></span>
<span data-ttu-id="75f0b-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="75f0b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75f0b-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="75f0b-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="75f0b-122">Parametro switch per disabilitare l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="75f0b-122">Switch parameter to disable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureDisableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f0b-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="75f0b-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="75f0b-124">Parametro switch per abilitare l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="75f0b-124">Switch parameter to enable auto update.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzureEnableAutoUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75f0b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="75f0b-125">-InputObject</span></span>
<span data-ttu-id="75f0b-126">Oggetto per il mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="75f0b-126">Object for protection container mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75f0b-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="75f0b-127">-Confirm</span></span>
<span data-ttu-id="75f0b-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75f0b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75f0b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75f0b-129">-WhatIf</span></span>
<span data-ttu-id="75f0b-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75f0b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75f0b-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="75f0b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75f0b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75f0b-132">CommonParameters</span></span>
<span data-ttu-id="75f0b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75f0b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75f0b-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75f0b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75f0b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="75f0b-135">INPUTS</span></span>

### <span data-ttu-id="75f0b-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="75f0b-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="75f0b-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="75f0b-137">OUTPUTS</span></span>

### <span data-ttu-id="75f0b-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="75f0b-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="75f0b-139">Note</span><span class="sxs-lookup"><span data-stu-id="75f0b-139">NOTES</span></span>

## <span data-ttu-id="75f0b-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="75f0b-140">RELATED LINKS</span></span>
