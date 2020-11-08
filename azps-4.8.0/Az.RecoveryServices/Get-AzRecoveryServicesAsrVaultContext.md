---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190149"
---
# <span data-ttu-id="0c8e7-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="0c8e7-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="0c8e7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8e7-103">Ottiene le informazioni sulle impostazioni del Vault ASR per il Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0c8e7-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="0c8e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c8e7-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c8e7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c8e7-105">DESCRIPTION</span></span>
<span data-ttu-id="0c8e7-106">Il cmdlet **Get-AzRecoveryServicesAsrVaultContext** ottiene le informazioni sulle impostazioni del Vault ASR correlate al Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0c8e7-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="0c8e7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c8e7-107">EXAMPLES</span></span>

### <span data-ttu-id="0c8e7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0c8e7-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="0c8e7-109">Ottiene le impostazioni del Vault ASR per il Vault dei servizi di ripristino attualmente attivo (nella sessione di PowerShell).</span><span class="sxs-lookup"><span data-stu-id="0c8e7-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="0c8e7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c8e7-110">PARAMETERS</span></span>

### <span data-ttu-id="0c8e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8e7-111">-DefaultProfile</span></span>
<span data-ttu-id="0c8e7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c8e7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c8e7-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8e7-113">CommonParameters</span></span>
<span data-ttu-id="0c8e7-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c8e7-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8e7-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c8e7-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8e7-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c8e7-116">INPUTS</span></span>

### <span data-ttu-id="0c8e7-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0c8e7-117">None</span></span>

## <span data-ttu-id="0c8e7-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c8e7-118">OUTPUTS</span></span>

### <span data-ttu-id="0c8e7-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="0c8e7-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="0c8e7-120">Note</span><span class="sxs-lookup"><span data-stu-id="0c8e7-120">NOTES</span></span>

## <span data-ttu-id="0c8e7-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c8e7-121">RELATED LINKS</span></span>
