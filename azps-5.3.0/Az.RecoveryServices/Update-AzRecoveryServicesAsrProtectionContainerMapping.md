---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 49c3fa6ec85f97c3c4010b6cfc9282933a844a6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474394"
---
# <span data-ttu-id="da420-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="da420-101">Update-AzRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="da420-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da420-102">SYNOPSIS</span></span>
<span data-ttu-id="da420-103">Aggiornare il mapping del contenitore di protezione del ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="da420-103">Update the Azure site recovery protection container mapping.</span></span>

## <span data-ttu-id="da420-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da420-104">SYNTAX</span></span>

### <span data-ttu-id="da420-105">AzureToAzureEnableAutoUpdate (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="da420-105">AzureToAzureEnableAutoUpdate (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-EnableAutoUpdate] -AutomationAccountId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da420-106">AzureToAzureDisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="da420-106">AzureToAzureDisableAutoUpdate</span></span>
```
Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-AzureToAzure] [-DisableAutoUpdate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da420-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da420-107">DESCRIPTION</span></span>
<span data-ttu-id="da420-108">Il cmdlet **Update-AzRecoveryServicesAsrProtectionContainerMapping** aggiorna il mapping del contenitore di protezione del ripristino del sito di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="da420-108">The **Update-AzRecoveryServicesAsrProtectionContainerMapping** cmdlet updates the specified Azure Site Recovery protection container mapping.</span></span>

## <span data-ttu-id="da420-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da420-109">EXAMPLES</span></span>

### <span data-ttu-id="da420-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="da420-110">Example 1</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping -AzureToAzure -DisableAutoUpdate
```

<span data-ttu-id="da420-111">Avviare l'operazione per disabilitare l'aggiornamento automatico per container.</span><span class="sxs-lookup"><span data-stu-id="da420-111">Start the operation to disable auto update for container.</span></span>

### <span data-ttu-id="da420-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="da420-112">Example 2</span></span>
```powershell
PS C:> Update-AzRecoveryServicesAsrProtectionContainerMapping -InputObject $ASRProtectionContainerMapping  -AzureToAzure -EnableAutoUpdate -AutomationAccountId $automationAccountId
```

<span data-ttu-id="da420-113">Avviare l'operazione per disabilitare Enable Auto Update per container.</span><span class="sxs-lookup"><span data-stu-id="da420-113">Start the operation to disable enable auto update for container.</span></span>

## <span data-ttu-id="da420-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da420-114">PARAMETERS</span></span>

### <span data-ttu-id="da420-115">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="da420-115">-AutomationAccountId</span></span>
<span data-ttu-id="da420-116">Specifica il accountId di automazione usato per la UDPATE automatica.</span><span class="sxs-lookup"><span data-stu-id="da420-116">Specifies the automation accountId used for auto udpate.</span></span>

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

### <span data-ttu-id="da420-117">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="da420-117">-AzureToAzure</span></span>
<span data-ttu-id="da420-118">Specifica Azure to Azure Protection container.</span><span class="sxs-lookup"><span data-stu-id="da420-118">Specifies Azure to Azure protection container.</span></span>

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

### <span data-ttu-id="da420-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da420-119">-DefaultProfile</span></span>
<span data-ttu-id="da420-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da420-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da420-121">-DisableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="da420-121">-DisableAutoUpdate</span></span>
<span data-ttu-id="da420-122">Parametro switch per disabilitare l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="da420-122">Switch parameter to disable auto update.</span></span>

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

### <span data-ttu-id="da420-123">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="da420-123">-EnableAutoUpdate</span></span>
<span data-ttu-id="da420-124">Parametro switch per abilitare l'aggiornamento automatico.</span><span class="sxs-lookup"><span data-stu-id="da420-124">Switch parameter to enable auto update.</span></span>

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

### <span data-ttu-id="da420-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="da420-125">-InputObject</span></span>
<span data-ttu-id="da420-126">Oggetto per il mapping del contenitore di protezione.</span><span class="sxs-lookup"><span data-stu-id="da420-126">Object for protection container mapping.</span></span>

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

### <span data-ttu-id="da420-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da420-127">-Confirm</span></span>
<span data-ttu-id="da420-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da420-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da420-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da420-129">-WhatIf</span></span>
<span data-ttu-id="da420-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da420-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da420-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da420-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da420-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da420-132">CommonParameters</span></span>
<span data-ttu-id="da420-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da420-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da420-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da420-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da420-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da420-135">INPUTS</span></span>

### <span data-ttu-id="da420-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="da420-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping</span></span>

## <span data-ttu-id="da420-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da420-137">OUTPUTS</span></span>

### <span data-ttu-id="da420-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="da420-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="da420-139">Note</span><span class="sxs-lookup"><span data-stu-id="da420-139">NOTES</span></span>

## <span data-ttu-id="da420-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da420-140">RELATED LINKS</span></span>
