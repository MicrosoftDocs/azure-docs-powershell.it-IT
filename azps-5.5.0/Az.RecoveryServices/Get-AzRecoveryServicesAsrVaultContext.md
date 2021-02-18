---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202030"
---
# <span data-ttu-id="18fb8-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="18fb8-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="18fb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="18fb8-102">SYNOPSIS</span></span>
<span data-ttu-id="18fb8-103">Recupera le informazioni delle impostazioni del Vault di Ripristino per il Vault di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="18fb8-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="18fb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18fb8-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18fb8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="18fb8-105">DESCRIPTION</span></span>
<span data-ttu-id="18fb8-106">Il cmdlet **Get-AzRecoveryServicesAsrVaultContext** ottiene le informazioni delle impostazioni del vault ASR relative al vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="18fb8-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="18fb8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18fb8-107">EXAMPLES</span></span>

### <span data-ttu-id="18fb8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="18fb8-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="18fb8-109">Recupera le impostazioni del vault ASR per il vault dei Servizi di ripristino attualmente attivi (nella sessione di PowerShell).</span><span class="sxs-lookup"><span data-stu-id="18fb8-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="18fb8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="18fb8-110">PARAMETERS</span></span>

### <span data-ttu-id="18fb8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18fb8-111">-DefaultProfile</span></span>
<span data-ttu-id="18fb8-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18fb8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18fb8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18fb8-113">CommonParameters</span></span>
<span data-ttu-id="18fb8-114">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18fb8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18fb8-115">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="18fb8-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18fb8-116">INPUT</span><span class="sxs-lookup"><span data-stu-id="18fb8-116">INPUTS</span></span>

### <span data-ttu-id="18fb8-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="18fb8-117">None</span></span>

## <span data-ttu-id="18fb8-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18fb8-118">OUTPUTS</span></span>

### <span data-ttu-id="18fb8-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="18fb8-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="18fb8-120">NOTE</span><span class="sxs-lookup"><span data-stu-id="18fb8-120">NOTES</span></span>

## <span data-ttu-id="18fb8-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18fb8-121">RELATED LINKS</span></span>
