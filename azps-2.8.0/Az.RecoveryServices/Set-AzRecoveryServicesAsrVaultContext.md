---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 846c27dc521e13cb2814a4f9e004325da4263bf7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855633"
---
# <span data-ttu-id="be685-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="be685-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="be685-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be685-102">SYNOPSIS</span></span>
<span data-ttu-id="be685-103">Imposta il contesto del Vault di servizi di ripristino da usare per le successive operazioni di ripristino dei siti di Azure nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="be685-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="be685-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be685-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be685-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be685-105">DESCRIPTION</span></span>
<span data-ttu-id="be685-106">Il cmdlet **set-AzRecoveryServicesAsrVaultContext** imposta il contesto di archiviazione del sito di ripristino di Azure per ulteriori operazioni.</span><span class="sxs-lookup"><span data-stu-id="be685-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="be685-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be685-107">EXAMPLES</span></span>

### <span data-ttu-id="be685-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be685-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="be685-109">Imposta il contesto del Vault nell'archivio di servizi di ripristino specificato per le successive operazioni di ripristino di Azure sito nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="be685-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="be685-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be685-110">PARAMETERS</span></span>

### <span data-ttu-id="be685-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be685-111">-DefaultProfile</span></span>
<span data-ttu-id="be685-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be685-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be685-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="be685-113">-Vault</span></span>
<span data-ttu-id="be685-114">Oggetto Vault di servizi di ripristino che corrisponde all'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="be685-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be685-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be685-115">-Confirm</span></span>
<span data-ttu-id="be685-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be685-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be685-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be685-117">-WhatIf</span></span>
<span data-ttu-id="be685-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be685-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be685-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be685-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be685-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be685-120">CommonParameters</span></span>
<span data-ttu-id="be685-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be685-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be685-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be685-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be685-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be685-123">INPUTS</span></span>

### <span data-ttu-id="be685-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="be685-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="be685-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be685-125">OUTPUTS</span></span>

### <span data-ttu-id="be685-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="be685-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="be685-127">Note</span><span class="sxs-lookup"><span data-stu-id="be685-127">NOTES</span></span>

## <span data-ttu-id="be685-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be685-128">RELATED LINKS</span></span>
