---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: c85d372ccd17b23fec46655245d050b668a32dc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514192"
---
# <span data-ttu-id="952ea-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="952ea-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="952ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="952ea-102">SYNOPSIS</span></span>
<span data-ttu-id="952ea-103">Imposta il contesto del Vault di servizi di ripristino da usare per le successive operazioni di ripristino dei siti di Azure nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="952ea-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="952ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="952ea-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="952ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="952ea-105">DESCRIPTION</span></span>
<span data-ttu-id="952ea-106">Il cmdlet **set-AzureRmRecoveryServicesAsrVaultContext** imposta il contesto di archiviazione del sito di ripristino di Azure per ulteriori operazioni.</span><span class="sxs-lookup"><span data-stu-id="952ea-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="952ea-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="952ea-107">EXAMPLES</span></span>

### <span data-ttu-id="952ea-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="952ea-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="952ea-109">Imposta il contesto del Vault nell'archivio di servizi di ripristino specificato per le successive operazioni di ripristino di Azure sito nella sessione corrente di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="952ea-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="952ea-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="952ea-110">PARAMETERS</span></span>

### <span data-ttu-id="952ea-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="952ea-111">-Confirm</span></span>
<span data-ttu-id="952ea-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="952ea-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952ea-113">-DefaultProfile</span></span>
<span data-ttu-id="952ea-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="952ea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952ea-115">-Vault</span><span class="sxs-lookup"><span data-stu-id="952ea-115">-Vault</span></span>
<span data-ttu-id="952ea-116">Oggetto Vault di servizi di ripristino che corrisponde all'archivio di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="952ea-116">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="952ea-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="952ea-117">-WhatIf</span></span>
<span data-ttu-id="952ea-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="952ea-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="952ea-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="952ea-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="952ea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952ea-120">CommonParameters</span></span>
<span data-ttu-id="952ea-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="952ea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952ea-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="952ea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952ea-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="952ea-123">INPUTS</span></span>

### <span data-ttu-id="952ea-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="952ea-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="952ea-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="952ea-125">OUTPUTS</span></span>

### <span data-ttu-id="952ea-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="952ea-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="952ea-127">Note</span><span class="sxs-lookup"><span data-stu-id="952ea-127">NOTES</span></span>

## <span data-ttu-id="952ea-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="952ea-128">RELATED LINKS</span></span>
