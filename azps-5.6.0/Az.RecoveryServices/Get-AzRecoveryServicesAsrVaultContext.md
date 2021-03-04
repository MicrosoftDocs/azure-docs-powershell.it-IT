---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 62f27b43158f8b01abc7be48cab93f4bb957258b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958078"
---
# <span data-ttu-id="afb15-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="afb15-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="afb15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afb15-102">SYNOPSIS</span></span>
<span data-ttu-id="afb15-103">Recupera le informazioni delle impostazioni del Vault di Ripristino per il Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="afb15-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="afb15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="afb15-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="afb15-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="afb15-105">DESCRIPTION</span></span>
<span data-ttu-id="afb15-106">Il cmdlet **Get-AzRecoveryServicesAsrVaultContext** ottiene le informazioni delle impostazioni del vault ASR relative al vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="afb15-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="afb15-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="afb15-107">EXAMPLES</span></span>

### <span data-ttu-id="afb15-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="afb15-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="afb15-109">Recupera le impostazioni del vault ASR per il vault dei Servizi di ripristino attualmente attivi (nella sessione di PowerShell).</span><span class="sxs-lookup"><span data-stu-id="afb15-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="afb15-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afb15-110">PARAMETERS</span></span>

### <span data-ttu-id="afb15-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb15-111">-DefaultProfile</span></span>
<span data-ttu-id="afb15-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="afb15-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afb15-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb15-113">CommonParameters</span></span>
<span data-ttu-id="afb15-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb15-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb15-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="afb15-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb15-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="afb15-116">INPUTS</span></span>

### <span data-ttu-id="afb15-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="afb15-117">None</span></span>

## <span data-ttu-id="afb15-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="afb15-118">OUTPUTS</span></span>

### <span data-ttu-id="afb15-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="afb15-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="afb15-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="afb15-120">NOTES</span></span>

## <span data-ttu-id="afb15-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="afb15-121">RELATED LINKS</span></span>
